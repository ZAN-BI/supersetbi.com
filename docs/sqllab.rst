..  Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

..    http://www.apache.org/licenses/LICENSE-2.0

..  Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

SQL Lab
=======

SQL Lab 是一个用 `React <https://facebook.github.io/react/>`_ 编写的功能丰富的现代 SQL IDE。

------

.. image:: images/screenshots/sqllab.png

------

功能概述
----------------
- 连接到几乎所有数据库后端
- 多标签环境可一次处理多个查询
- 利用 Superset 丰富的可视化功能，流畅地可视化查询结果
- 浏览数据库元数据：表，列，索引，分区
- 支持长时间运行的查询

  - 使用 `Celery distributed queue <http://www.celeryproject.org/>`_
    去分发查询处理到 workers
  - 支持定义一个 "results backend" 以保留查询结果

- 一个搜索引擎去查找过去执行的查询
- 支持使用 `Jinja templating language <http://jinja.pocoo.org/docs/dev/>`_ 进行模板，该语言允许在 SQL 代码中使用宏

额外功能
--------------
- 敲击 ``alt + enter`` 来作为键盘快捷方式去运行你的查询

用 Jinja 制作模板
---------------------

.. code-block:: sql

    SELECT *
    FROM some_table
    WHERE partition_key = '{{ presto.first_latest_partition('some_table') }}'

模板释放了 SQ L代码中编程语言的强大功能。

模板还可用于编写已参数化的通用查询，以便可以轻松地重用它们。


可用的宏
''''''''''''''''
我们在 Superset 的 Jinja 上下文中公开了 Python 标准库中的某些模块:

- ``time``: ``time``
- ``datetime``: ``datetime.datetime``
- ``uuid``: ``uuid``
- ``random``: ``random``
- ``relativedelta``: ``dateutil.relativedelta.relativedelta``

`Jinja's builtin filters <http://jinja.pocoo.org/docs/dev/templates/>`_ 也可以应用在需要的地方。

.. autofunction:: superset.jinja_context.current_user_id

.. autofunction:: superset.jinja_context.current_username

.. autofunction:: superset.jinja_context.url_param

.. autofunction:: superset.jinja_context.filter_values

.. autofunction:: superset.jinja_context.CacheKeyWrapper.cache_key_wrapper

.. autoclass:: superset.jinja_context.PrestoTemplateProcessor
    :members:

.. autoclass:: superset.jinja_context.HiveTemplateProcessor
    :members:

扩展的宏
''''''''''''''''

正如 `Installation & Configuration <https://superset.incubator.apache.org/installation.html#installation-configuration>`_ 文档中提到的，
管理员可以使用配置变量 ``JINJA_CONTEXT_ADDONS`` 在其环境中公开更多的宏。
本字典中引用的所有对象都可以在 **SQL Lab** 中集成到用户的查询中。

查询成本估算
'''''''''''''''''''''

一些数据库支持 ``EXPLAIN`` 查询，这些查询使用户可以在执行此操作之前估算查询的成本。
当前，SQL Lab 支持 Presto。要启用查询成本估算，请将以下键添加到数据库配置中的 "Extra" 字段中：

.. code-block:: text

    {
        "version": "0.319",
        "cost_estimate_enabled": true
        ...
    }

在这里，"version" 应该是 Presto cluster 的版本。Presto 0.319 中引入了对此功能的支持。

您还需要在 `superset_config.py` 中启用功能标记，并且可以选择指定自定义格式器。 例如：

.. code-block:: python

    def presto_query_cost_formatter(cost_estimate: List[Dict[str, float]]) -> List[Dict[str, str]]:
        """
        Format cost estimate returned by Presto.

        :param cost_estimate: JSON estimate from Presto
        :return: Human readable cost estimate
        """
        # Convert cost to dollars based on CPU and network cost. These coefficients are just
        # examples, they need to be estimated based on your infrastructure.
        cpu_coefficient = 2e-12
        network_coefficient = 1e-12

        cost = 0
        for row in cost_estimate:
            cost += row.get("cpuCost", 0) * cpu_coefficient
            cost += row.get("networkCost", 0) * network_coefficient

        return [{"Cost": f"US$ {cost:.2f}"}]


    DEFAULT_FEATURE_FLAGS = {
        "ESTIMATE_QUERY_COST": True,
        "QUERY_COST_FORMATTERS_BY_ENGINE": {"presto": presto_query_cost_formatter},
    }

.. _ref_ctas_engine_config:

创建表为 (CTAS)
''''''''''''''''''''''

您可以在 SQLLab 上使用 ``CREATE TABLE AS SELECT ...`` 语句。可以在数据库配置级别上启用和禁用此功能。

请注意，由于 ``CREATE TABLE..`` 属于 SQL DDL 类别。特别是在 PostgreSQL 上，DDL 是事务性的，
这意味着要正确使用此功能，必须在 engine 参数上将 ``autocommit`` 设置为true：

.. code-block:: text

    {
        ...
        "engine_params": {"isolation_level":"AUTOCOMMIT"},
        ...
    }
