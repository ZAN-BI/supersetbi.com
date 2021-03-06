# Contributing

贡献

Contributions are welcome and are greatly appreciated! Every
little bit helps, and credit will always be given.

欢迎投稿，我们将不胜感激! 每一点都有帮助，荣誉总是会被给予。
* contributing adj. 贡献的；起作用的
* contribution n. 贡献；捐献；投稿
* greatly adv.非常;很;大大地
* appreciate v.欣赏;赏识;重视;感激;感谢;欢迎;理解;意识到;领会

## Table of Contents

- [Contributing](#contributing)
  - [Table of Contents](#table-of-contents)
  - [Orientation](#orientation)
  - [Types of Contributions](#types-of-contributions)
    - [Report Bug](#report-bug)
    - [Submit Ideas or Feature Requests](#submit-ideas-or-feature-requests)
    - [Fix Bugs](#fix-bugs)
    - [Implement Features](#implement-features)
    - [Improve Documentation](#improve-documentation)
    - [Add Translations](#add-translations)
    - [Ask Questions](#ask-questions)
  - [Pull Request Guidelines](#pull-request-guidelines)
    - [Protocol](#protocol)
      - [Authoring](#authoring)
      - [Reviewing](#reviewing)
      - [Merging](#merging)
      - [Post-merge Responsibility](#post-merge-responsibility)
  - [Managing Issues and PRs](#managing-issues-and-prs)
  - [Revert Guidelines](#revert-guidelines)
  - [Setup Local Environment for Development](#setup-local-environment-for-development)
    - [Documentation](#documentation)
      - [Images](#images)
      - [API documentation](#api-documentation)
    - [Flask server](#flask-server)
      - [OS Dependencies](#os-dependencies)
      - [Logging to the browser console](#logging-to-the-browser-console)
    - [Frontend Assets](#frontend-assets)
      - [nvm and node](#nvm-and-node)
      - [Prerequisite](#prerequisite)
      - [Installing Dependencies](#installing-dependencies)
      - [Building](#building)
      - [Docker (docker-compose)](#docker-docker-compose)
      - [Updating NPM packages](#updating-npm-packages)
      - [Feature flags](#feature-flags)
  - [Git Hooks](#git-hooks)
  - [Linting](#linting)
  - [Conventions](#conventions)
    - [Python](#python)
  - [Typing](#typing)
    - [Python](#python-1)
    - [TypeScript](#typescript)
  - [Testing](#testing)
    - [Python Testing](#python-testing)
    - [Frontend Testing](#frontend-testing)
    - [Integration Testing](#integration-testing)
  - [Translating](#translating)
    - [Enabling language selection](#enabling-language-selection)
    - [Extracting new strings for translation](#extracting-new-strings-for-translation)
    - [Creating a new language dictionary](#creating-a-new-language-dictionary)
  - [Tips](#tips)
    - [Adding a new datasource](#adding-a-new-datasource)
    - [Creating a new visualization type](#creating-a-new-visualization-type)
    - [Adding a DB migration](#adding-a-db-migration)
    - [Merging DB migrations](#merging-db-migrations)
    - [SQL Lab Async](#sql-lab-async)
  - [Chart Parameters](#chart-parameters)
    - [Datasource & Chart Type](#datasource--chart-type)
    - [Time](#time)
    - [GROUP BY](#group-by)
    - [NOT GROUPED BY](#not-grouped-by)
    - [Y Axis 1](#y-axis-1)
    - [Y Axis 2](#y-axis-2)
    - [Query](#query)
    - [Filters Configuration](#filters-configuration)
    - [Options](#options)
    - [Chart Options](#chart-options)
    - [X Axis](#x-axis)
    - [Y Axis](#y-axis)
    - [Other](#other)
    - [Unclassified](#unclassified)

## Orientation

方向
* orientation n. 方向；定向；适应；情况介绍；向东方

Here's a list of repositories that contain Superset-related packages:

下面是包含与 Superset 相关的包的存储库列表:

- [apache/incubator-superset](https://github.com/apache/incubator-superset)
  is the main repository containing the `apache-superset` Python package
  distributed on
  [pypi](https://pypi.org/project/apache-superset/). This repository
  also includes Superset's main TypeScript/JavaScript bundles and react apps under
  the [superset-frontend](https://github.com/apache/incubator-superset/tree/master/superset-frontend)
  folder.
  * [apache/incubator-superset](https://github.com/apache/incubator-superset) 是主存储库，
  其中包含分发在 pypi 上的apache-superset Python 包。
  这个资源库还包括 Superset 的主要 TypeScript/JavaScript 包，
  以及在 [superset-frontend](https://github.com/apache/incubator-superset/tree/master/superset-frontend) 
  文件夹下的 react 应用。

- [apache-superset/superset-ui](https://github.com/apache-superset/superset-ui)
  contains core Superset's
  [npm packages](https://github.com/apache-superset/superset-ui/tree/master/packages).
  These packages are shared across the React apps in the main repository,
  and in visualization plugins.
  * [apache-superset/superset-ui](https://github.com/apache-superset/superset-ui) 包含核心
  Superset 的 npm 包。这些包在主存储库中的 React 应用程序和可视化插件中共享。

- [apache-superset/superset-ui-plugins](https://github.com/apache-superset/superset-ui-plugins)
  contains the code for the default visualizations that ship with Superset
  and are maintained by the core community.
  * [apache-superset/superset-ui-plugins](https://github.com/apache-superset/superset-ui-plugins)
  包含了 Superset 附带的、由核心社区维护的默认可视化的代码。

- [apache-superset/superset-ui-plugins-deckgl](https://github.com/apache-superset/superset-ui-plugins-deckgl)
  contains the code for the geospatial visualizations that ship with Superset
  and are maintained by the core community.
  * [apache-superset/superset-ui-plugins-deckgl](https://github.com/apache-superset/superset-ui-plugins-deckgl)
  包含了随 Superset 一起发布并由核心社区维护的地理空间可视化代码。

- [github.com/apache-superset](https://github.com/apache-superset) is the
  Github organization under which we manage Superset-related
  small tools, forks and Superset-related experimental ideas.
  * [github.com/apache-superset](https://github.com/apache-superset) 是 Github 组织，
  我们在该组织下管理与 Superset 相关的小工具、分叉和与 Superset 相关的实验想法。
    * experimental adj. 实验的；根据实验的；试验性的

## Types of Contributions

贡献类型

### Report Bug

上报 Bug

The best way to report a bug is to file an issue on GitHub. Please include:

报告 bug 的最佳方法是在 GitHub 上提交一个 issue。请包括:

- Your operating system name and version.
  * 您的操作系统名称和版本。
- Superset version.
  * Superset 版本
- Detailed steps to reproduce the bug.
  * 重现错误的详细步骤。
    * reproduce vt. 复制；再生；生殖；使…在脑海中重现
- Any details about your local setup that might be helpful in troubleshooting.
  * 有关您的本地设置的任何可能有助于故障排除的细节。

When posting Python stack traces, please quote them using
[Markdown blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/).

在发布 Python 堆栈跟踪时，请使用 [Markdown blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks/)
引用它们。

### Submit Ideas or Feature Requests

提交想法或特性请求

The best way is to file an issue on GitHub:

最好的办法是在 GitHub 上提交一个问题:

- Explain in detail how it would work.
  * 详细解释它是如何工作的。
- Keep the scope as narrow as possible, to make it easier to implement.
  * 保持范围尽可能小，以便更容易实现。
    * narrow adj. 狭窄的，有限的；勉强的；精密的；度量小的
- Remember that this is a volunteer-driven project, and that contributions are welcome :)
  * 请记住，这是一个由志愿者推动的项目，欢迎大家贡献自己的力量。
    * volunteer n. 志愿者；志愿兵

For large features or major changes to codebase, please create **Superset Improvement Proposal (SIP)**. See template from [SIP-0](https://github.com/apache/incubator-superset/issues/5602)

对于较大的特性或对代码库的主要更改，请创建 **Superset 改进建议(SIP)**。参见 [SIP-0](https://github.com/apache/incubator-superset/issues/5602) 中的模板

### Fix Bugs

Bug 修复

Look through the GitHub issues. Issues tagged with `#bug` are
open to whoever wants to implement them.

浏览 GitHub 的 issues。标记为 `#bug` 的 issues 对任何想要实现它们的人都是开放的。
  * whoever pron.…的那个人(或那些人);…的任何人;无论谁;不管什么人;(用于问句，表示惊讶)究竟是谁，到底是谁

### Implement Features

实现功能

Look through the GitHub issues. Issues tagged with
`#feature` is open to whoever wants to implement it.

查看 GitHub issues。带有 `#feature` 标签的 issues 对任何想要实现它的人都是开放的。
  * Look through 逐一查看; 浏览; 翻阅

### Improve Documentation

改进文档

Superset could always use better documentation,
whether as part of the official Superset docs,
in docstrings, `docs/*.rst` or even on the web as blog posts or
articles. See [Documentation](#documentation) for more details.

Superset 总是可以使用更好的文档，
无论是作为官方 Superset 文档的一部分，
还是在 docstrings, `docs/*.rst` 中。
甚至在 web 上作为博客帖子或文章。有关更多细节，请参见 [Documentation](#documentation)。

### Add Translations

添加翻译

If you are proficient in a non-English language, you can help translate
text strings from Superset's UI. You can jump in to the existing
language dictionaries at
`superset/translations/<language_code>/LC_MESSAGES/messages.po`, or
even create a dictionary for a new language altogether.
See [Translating](#translating) for more details.

如果你精通非英语语言，你可以帮助翻译 Superset 用户界面中的文本字符串。
您可以通过 `superset/translations/<language_code>/LC_MESSAGES/messages.po` 跳转到现有的语言词典。
或者干脆为一门新语言创建一本词典。有关更多细节，请参见 [Translating](#translating)。
* proficient in 精通; 熟练

### Ask Questions

提出问题

There is a dedicated [`apache-superset` tag](https://stackoverflow.com/questions/tagged/apache-superset) on [StackOverflow](https://stackoverflow.com/). Please use it when asking questions.

[StackOverflow](https://stackoverflow.com/) 上有一个专用的 [`apache-superset` tag](https://stackoverflow.com/questions/tagged/apache-superset)。请在提问时使用。

## Pull Request Guidelines

PR 指南

A philosophy we would like to strongly encourage is

我们强烈提倡的一种哲学是
* philosophy n. 哲学；哲理；人生观

> Before creating a PR, create an issue.

创建 PR 之前，请先创建 issue。

The purpose is to separate problem from possible solutions.

其目的是将问题与可能的解决方案分开。

**Bug fixes:** If you’re only fixing a small bug, it’s fine to submit a pull request right away but we highly recommend to file an issue detailing what you’re fixing. This is helpful in case we don’t accept that specific fix but want to keep track of the issue. Please keep in mind that the project maintainers reserve the rights to accept or reject incoming PRs, so it is better to separate the issue and the code to fix it from each other. In some cases, project maintainers may request you to create a separate issue from PR before proceeding.

**Bug 修复：** 如果你只是修复了一个小 bug，那么立即提交一个 pull request 是可以的，但是我们强烈建议你提交一个 issue，详细说明你正在修复的问题。如果我们不接受特定的修复，但希望跟踪这个 issue，这将很有帮助。请记住，项目维护者保留接受或拒绝传入 PRs 的权利，所以最好将问题和修复它的代码分开。在某些情况下，项目维护者可能会要求您在继续之前创建一个独立于 PR 的问题。
* right away 立刻
* keep track of 跟上…的进展;掌握…的最新消息
* each other 互相，彼此
* proceeding
  * n. 进行；程序；诉讼；事项
  * v. 开始；继续做；行进（proceed的ing形式）

**Refactor:** For small refactors, it can be a standalone PR itself detailing what you are refactoring and why. If there are concerns, project maintainers may request you to create a `#SIP` for the PR before proceeding.

**重构：** 对于小的重构，它可以是一个独立的 PR 本身，详细说明您要重构的内容和原因。如果有问题，项目维护人员可能会要求您在继续之前为 PR 创建一个 `#SIP`。
* standalone adj.单独的，独立的

**Feature/Large changes:** If you intend to change the public API, or make any non-trivial changes to the implementation, we requires you to file a new issue as `#SIP` (Superset Improvement Proposal). This lets us reach an agreement on your proposal before you put significant effort into it. You are welcome to submit a PR along with the SIP (sometimes necessary for demonstration), but we will not review/merge the code until the SIP is approved.

**特性/大变化：** 如果您打算更改公共 API，或者对实现进行任何重要的更改，我们要求您提交一个新 issue 作为 `#SIP` ( Superset 改进建议)。这使我们能够在你作出重大努力之前就你的建议达成协议。欢迎您与 SIP 一起提交一份 PR (有时需要进行演示)，但是在 SIP 得到批准之前，我们不会 review/merge 代码。
* intend to 打算; 打算去; 想要
* reach an agreement 达成协议
* along with 除某物以外; 随同…一起，跟…一起
* necessary for 对…是必要的

In general, small PRs are always easier to review than large PRs. The best practice is to break your work into smaller independent PRs and refer to the same issue. This will greatly reduce turnaround time.

一般来说，小 PRs 总是比大 PRs 更容易审查。最好的做法是把你的工作分解成更小的独立的PRs，并参考相同的 issue。这将大大减少周转时间。

Finally, never submit a PR that will put master branch in broken state. If the PR is part of multiple PRs to complete a large feature and cannot work on its own, you can create a feature branch and merge all related PRs into the feature branch before creating a PR from feature branch to master.

最后，永远不要提交会使主分支处于崩溃状态的 PR。如果 PR 是多个 PRs 的一部分，以完成一个大的功能，而不能单独工作，你可以创建一个功能分支，并将所有相关的 PRs 合并到功能分支中，然后再创建一个从功能分支到主功能分支的 PR。

### Protocol

协议

#### Authoring

编写

- Fill in all sections of the PR template.
- 填写 PR 模板的所有部分。

- Add prefix `[WIP]` to title if not ready for review (WIP = work-in-progress). We recommend creating a PR with `[WIP]` first and remove it once you have passed CI test and read through your code changes at least once.
- 如果没有准备好 review，则在标题中添加前缀 `[WIP]` (WIP = work-in-progress)。我们建议首先创建一个带有 `[WIP]` 的 PR，并在通过 CI 测试并至少阅读一次代码更改之后删除它。

- **Screenshots/GIFs:** Changes to user interface require before/after screenshots, or GIF for interactions
  - Recommended capture tools ([Kap](https://getkap.co/), [LICEcap](https://www.cockos.com/licecap/), [Skitch](https://download.cnet.com/Skitch/3000-13455_4-189876.html))
  - If no screenshot is provided, the committers will mark the PR with `need:screenshot` label and will not review until screenshot is provided.
- **屏幕截图/GIF：** 更改用户界面需要在屏幕截图之前/之后进行，或更改 GIF 以进行交互
  - 推荐的捕获工具 ([Kap](https://getkap.co/), [LICEcap](https://www.cockos.com/licecap/), [Skitch](https://download.cnet.com/Skitch/3000-13455_4-189876.html))
  - 如果没有提供截图，提交者将在 PR 上标注 `need:screenshot` 的标签，在提供截图之前不会进行审查。

- **Dependencies:** Be careful about adding new dependency and avoid unnecessary dependencies.
  - For Python, include it in `setup.py` denoting any specific restrictions and in `requirements.txt` pinned to a specific version which ensures that the application build is deterministic.
  - For TypeScript/JavaScript, include new libraries in `package.json`
- **依赖关系：** 添加新的依赖项时要小心，避免不必要的依赖项。
  - 对于 Python，将其包含在表示任何特定限制的 `setup.py` 和固定到特定版本的 `requirements.txt` 中，以确保应用程序生成是确定的。
    * denoting v.标志;预示;象征;表示;意指 denote的现在分词
    * pinned v.(用大头钉等)固定，别上，钉住;使不能动弹;按住;钳住 pin的过去分词和过去式
    * restrictions n.限制规定;限制法规;限制;约束;制约因素 restriction的复数
    * deterministic adj. 确定性的；命运注定论的
  - 对于 TypeScript/JavaScript，在 'package.json' 中包含新库

- **Tests:** The pull request should include tests, either as doctests, unit tests, or both. Make sure to resolve all errors and test failures. See [Testing](#testing) for how to run tests.
- **测试：** pull request 应该包括测试，或者作为文档测试，或者单元测试，或者两者都包含。确保解决所有的错误和测试失败。有关如何运行测试，请参见 [Testing](#testing)。

- **Documentation:** If the pull request adds functionality, the docs should be updated as part of the same PR. Doc string are often sufficient, make sure to follow the sphinx compatible standards.
- **文档：** 如果 pull request 添加了功能，文档应该作为相同 PR 的一部分进行更新。Doc 字符串通常就足够了，请确保遵循 sphinx 兼容标准。
  * compatible adj.可共用的;兼容的;可共存的;(因志趣等相投而)关系好的，和睦相处的
  * sufficient adj.足够的;充足的
  * functionality n.实用;符合实际;设计目的;设计功能;(计算机或电子系统的)功能

- **CI:** Reviewers will not review the code until all CI tests are passed. Sometimes there can be flaky tests. You can close and open PR to re-run CI test. Please report if the issue persists. After the CI fix has been deployed to `master`, please rebase your PR.
- **持续集成：** 在通过所有 CI 测试之前，评审员不会评审代码。有时会有不可靠的测试。您可以关闭和打开 PR 来重新运行CI 测试。如果问题仍然存在，请报告。在 CI 修复被部署到 `master` 之后，请重新调整您的 PR。
  * flaky adj. 薄片的；薄而易剥落的；古里古怪的
  * persist vi. 存留，坚持；持续，固执

- **Code coverage:** Please ensure that code coverage does not decrease.
- Remove `[WIP]` when ready for review. Please note that it may be merged soon after approved so please make sure the PR is ready to merge and do not expect more time for post-approval edits.
- If the PR was not ready for review and inactive for > 30 days, we will close it due to inactivity. The author is welcome to re-open and update.
- **代码覆盖率：** 请确保代码覆盖率不会降低。
- 在准备评审时删除 `[WIP]`。请注意，审批后不久可能会合并，因此请确保 PR 已准备好合并，并且不要期望有更多时间进行审批后编辑。
- 如果 PR 未准备好供审阅，并且在超过 30 天内处于不活动状态，我们将由于不活动而关闭它。欢迎作者重新打开和更新。

#### Reviewing

审查

- Use constructive tone when writing reviews.
- If there are changes required, state clearly what needs to be done before the PR can be approved.
- If you are asked to update your pull request with some changes there's no need to create a new one. Push your changes to the same branch.
- The committers reserve the right to reject any PR and in some cases may request the author to file an issue.

- 写评论时要用建设性的语气。
  * constructive adj.建设性的;有助益的;积极的
  * tone n.语气;口气;腔调;
- 如果需要更改，请清楚说明在批准 PR 之前需要做什么。
- 如果你被要求更新你的 pull request 使用一些变化，没有必要创建一个新的。将更改推到同一分支。
- 提交人保留拒绝任何 PR 的权利，在某些情况下可能会要求作者提交 issue。

#### Merging

合并

- At least one approval is required for merging a PR.
- PR is usually left open for at least 24 hours before merging.
- After the PR is merged, [close the corresponding issue(s)](https://help.github.com/articles/closing-issues-using-keywords/).

- 合并 PR 至少需要一个审批。
- PR 通常在合并前至少24小时保持打开状态。
- PR 合并后，[关闭相应问题](https://help.github.com/articles/closing-issues-using-keywords/)。
  * corresponding adj.符合的;相应的;相关的

#### Post-merge Responsibility

合并后责任

- Project maintainers may contact the PR author if new issues are introduced by the PR.
- Project maintainers may revert your changes if a critical issue is found, such as breaking master branch CI.

- 如果PR引入了新问题，项目维护人员可以联系PR作者。
- 如果发现关键问题（如中断主分支 CI），项目维护人员可能会还原您的更改。
  * critical adj.批评的;批判性的;挑剔的;极重要的;关键的;至关紧要的;严重的;不稳定的;可能有危险的
  * revert vt. 使恢复原状

## Managing Issues and PRs

管理 Issues 和 PRs

To handle issues and PRs that are coming in, committers read issues/PRs and flag them with labels to categorize and help contributors spot where to take actions, as contributors usually have different expertises.

为了处理即将到来的 issues 和 PRs，
提交者阅读 issues/PRs 并用 labels 标记它们，
以便对贡献者进行分类
并帮助贡献者确定采取行动的位置，
因为贡献者通常具有不同的专业知识。
* expertise n. 专门知识；专门技术；专家的意见
* spot adv. 准确地；恰好

Triaging goals

筛选目标

- **For issues:** Categorize, screen issues, flag required actions from authors.
- **For PRs:** Categorize, flag required actions from authors. If PR is ready for review, flag required actions from reviewers.

- **针对 issues:** 分类，筛选问题，标记需要作者执行的操作。
- **针对 PRs:** 分类，标记来自作者的必需操作。如果 PR 已准备好进行评审，则标记评审员所需的操作。

First, add **Category labels (a.k.a. hash labels)**. Every issue/PR must have one hash label (except spam entry). Labels that begin with `#` defines issue/PR type:

首先，添加 **分类标签  (a.k.a. hash 标签)**。每个 issue/PR 必须有一个 hash 标签（除了垃圾邮件条目）。

| Label           | for Issue                                                                                                                               | for PR                                                                                                                                            |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `#bug`          | Bug report                                                                                                                              | Bug fix                                                                                                                                           |
| `#code-quality` | Describe problem with code, architecture or productivity                                                                                | Refactor, tests, tooling                                                                                                                          |
| `#feature`      | New feature request                                                                                                                     | New feature implementation                                                                                                                        |
| `#refine`       | Propose improvement that does not provide new features and is also not a bug fix nor refactor, such as adjust padding, refine UI style. | Implementation of improvement that does not provide new features and is also not a bug fix nor refactor, such as adjust padding, refine UI style. |
| `#doc`          | Documentation                                                                                                                           | Documentation                                                                                                                                     |
| `#question`     | Troubleshooting: Installation, Running locally, Ask how to do something. Can be changed to `#bug` later.                                | N/A                                                                                                                                               |
| `#SIP`          | Superset Improvement Proposal                                                                                                           | N/A                                                                                                                                               |
| `#ASF`          | Tasks related to Apache Software Foundation policy                                                                                      | Tasks related to Apache Software Foundation policy                                                                                                |
---
---
---

| 标签           | 针对 Issue                                                                                                                               | 针对 PR                                                                                                                                            |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| `#bug`          | Bug 上报                                                                                                                              | Bug 修复                                                                                                                                           |
| `#code-quality` | 描述代码、架构或生产效率方面的问题                                                                                | 重构、测试、工具                                                                                                                         |
| `#feature`      | 新功能请求                                                                                                                   | 新功能实现                                                                                              |
| `#refine`       | 不提供新特性的改进，也不是bug修复或重构，比如调整填充、改进UI样式。 | 实现的改进，不提供新的功能，也不是一个 bug 修复或重构，如调整填充，细化UI风格。|
| `#doc`          | 文档                                                                                                                           | 文档                                                                                                                                     |
| `#question`     | 故障排除: 安装，本地运行，询问如何做某事。稍后可以更改为`#bug`。                                | N/A                                                                                                                                               |
| `#SIP`          | Superset 改进建议                                                                                                           | N/A                                                                                                                                               |
| `#ASF`          | 与 Apache Software Foundation 策略相关的任务                                                                                      | 与Apache Software Foundation策略相关的任务                                                                                                |


Then add other types of labels as appropriate.

然后根据需要添加其他类型的标签。

- **Descriptive labels (a.k.a. dot labels):** These labels that begin with `.` describe the details of the issue/PR, such as `.ui`, `.js`, `.install`, `.backend`, etc. Each issue/PR can have zero or more dot labels.
- **描述性标签 (a.k.a. 点标签):** 这些标签以 `.` 开始描述 issue/PR 的详细信息，例如 `.ui`, `.js`, `.install`, `.backend` 等。每个 issue/PR 可以有零个或多个点标签。
- **Need labels:** These labels have pattern `need:xxx`, which describe the work required to progress, such as `need:rebase`, `need:update`, `need:screenshot`.
- **需要标签:** 这些标签有 `need:xxx` 模式，描述了需要进行的工作，像 `need:rebase`, `need:update`, `need:screenshot`。
- **Risk labels:** These labels have pattern `risk:xxx`, which describe the potential risk on adopting the work, such as `risk:db-migration`. The intention was to better understand the impact and create awareness for PRs that need more rigorous testing.
- **风险标签:** 这些标签有 `risk:xxx` 模式，描述采用该工作的潜在风险，如 `risk:db-migration`。其目的是为了更好地理解影响，并为需要更严格测试的 PRs 创建感知。
- **Status labels:** These labels describe the status (`abandoned`, `wontfix`, `cant-reproduce`, etc.) Issue/PRs that are rejected or closed without completion should have one or more status labels.
- **状态标签:** 这些标签描述了被拒绝或未完成就关闭的 Issue/PRs(`abandoned`, `wontfix`, `cant-reproduce`, 等.) 状态 ，应该有一个或多个状态标签。
- **Version labels:** These have the pattern `vx.x` such as `v0.28`. Version labels on issues describe the version the bug was reported on. Version labels on PR describe the first release that will include the PR.
- **版本标签:** 这些有 `vx.x` 模式，例如 `v0.28`。issues 上的版本标签描述了报告错误的版本。PR 上的版本标签描述了包含 PR 的第一个版本。

Committers may also update title to reflect the issue/PR content if the author-provided title is not descriptive enough.

如果作者提供的标题不够描述性，提交者也可以更新标题来反映 issue/PR 内容。

If the PR passes CI tests and does not have any `need:` labels, it is ready for review, add label `review` and/or `design-review`.

如果 PR 通过了 CI 测试，并且没有任何 `need:` 标签，那么它就可以进行评审了，添加 `review` 和/或 `design-review` 标签。

If an issue/PR has been inactive for >=30 days, it will be closed. If it does not have any status label, add `inactive`.

如果一个 issue/PR 在 >=30 天内处于非活动状态，那么它将被关闭。如果它没有任何状态标签，添加 `inactive`。

## Revert Guidelines

恢复指南

Reverting changes that are causing issues in the master branch is a normal and expected part of the development process. In an open source community, the ramifications of a change cannot always be fully understood. With that in mind, here are some considerations to keep in mind when considering a revert:

恢复主分支中引起问题的更改是开发过程中正常的和预期的一部分。在开放源码社区中，更改的结果并不总是能够被完全理解。考虑到这一点，以下是在考虑恢复时需要注意的一些事项:
* ramification n. 衍生物；分枝，分叉；支流；（衍生的）结果、影响
* considerations n. 考虑；注意事项（consideration的复数形式）；体贴
* keep in mind 牢记;放在心上
* considering prep. 考虑到；就...而论

- **Availability of the PR author:** If the original PR author or the engineer who merged the code is highly available and can provide a fix in a reasonable timeframe, this would counter-indicate reverting.
- **PR 作者的可用性:** 如果原始的 PR 作者或合并代码的工程师是高度可用的，并且可以在合理的时间范围内提供修复，则这将反向指示恢复。
- **Severity of the issue:** How severe is the problem on master? Is it keeping the project from moving forward? Is there user impact? What percentage of users will experience a problem?
- **issue 的严重程度:** master 的问题有多严重？是不是妨碍了项目的进展？对用户有影响吗？有多少百分比的用户会遇到问题？
- **Size of the change being reverted:** Reverting a single small PR is a much lower-risk proposition than reverting a massive, multi-PR change.
- **正在还原的更改的大小:** 恢复一个小的 PR 比恢复一个大的、多 PR 变化的风险要低得多。
- **Age of the change being reverted:** Reverting a recently-merged PR will be more acceptable than reverting an older PR. A bug discovered in an older PR is unlikely to be causing widespread serious issues.
- **正在还原的更改的时间：** 恢复最近合并的PR将比恢复旧的PR更容易被接受。在旧的PR中发现的 bug 不太可能引起广泛的严重问题。
- **Risk inherent in reverting:** Will the reversion break critical functionality? Is the medicine more dangerous than the disease?
- **还原的内在风险:** 降级会破坏关键功能吗?药物比疾病更危险吗?
- **Difficulty of crafting a fix:** In the case of issues with a clear solution, it may be preferable to implement and merge a fix rather than a revert.
- **修复的难度：** 对于具有明确解决方案的问题，最好是实现并合并修复，而不是恢复。

Should you decide that reverting is desirable, it is the responsibility of the Contributor performing the revert to:

如果您认为恢复是可取的，则执行恢复的参与者有责任：

- **Contact the interested parties:** The PR's author and the engineer who merged the work should both be contacted and informed of the revert.
- **Provide concise reproduction steps:** Ensure that the issue can be clearly understood and duplicated by the original author of the PR.
- **Put the revert through code review:** The revert must be approved by another committer.

- **联系相关方：** 应联系 PR 的作者和合并工作的工程师，并告知其还原。
- **提供简洁的复制步骤:** 确保问题能够被原PR作者清楚地理解和复制。
- **通过代码检查还原：** 还原必须由另一个提交者批准。

## Setup Local Environment for Development

设置本地开发环境

First, [fork the repository on GitHub](https://help.github.com/articles/about-forks/), then clone it. You can clone the main repository directly, but you won't be able to send pull requests.

首先，[在 GitHub 上 fork 这个仓库](https://help.github.com/articles/about-forks/)，然后 clone 它。你可以直接克隆这个主仓库，但是你没有能力发送 PR。

```bash
git clone git@github.com:your-username/incubator-superset.git
cd incubator-superset
```

### Documentation

文档

The latest documentation and tutorial are available at https://superset.incubator.apache.org/.

最新的文档和教程可以在 https://superset.incubator.apache.org/ 上找到。

Contributing to the official documentation is relatively easy, once you've setup
your environment and done an edit end-to-end. The docs can be found in the
`docs/` subdirectory of the repository, and are written in the
[reStructuredText format](https://en.wikipedia.org/wiki/ReStructuredText) (.rst).
If you've written Markdown before, you'll find the reStructuredText format familiar.

一旦您设置了环境并完成了端到端的编辑，就可以相对容易地为官方文档做贡献。文档可以在存储库的 `docs/` 子目录中找到，并以 [reStructuredText 格式](https://en.wikipedia.org/wiki/ReStructuredText) (.rst) 编写。如果您以前写过Markdown，您会发现 reStructuredText 格式很熟悉。

Superset 使用 [Sphinx](http://www.sphinx-doc.org/en/1.5.1/) 将 `docs/` 中的 rst 文件转换为用户看到的最终 HTML 输出。

Finally, to make changes to the rst files and build the docs using Sphinx,
you'll need to install a handful of dependencies from the repo you cloned:

最后，要更改 rst 文件并使用 Sphinx 构建文档，需要从克隆的 repo 中安装一些依赖项：

```bash
pip install -r docs/requirements.txt
```

To get the feel for how to edit and build the docs, let's edit a file, build
the docs and see our changes in action. First, you'll want to
[create a new branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
to work on your changes:

为了了解如何编辑和构建文档，让我们编辑一个文件，构建文档并查看我们的更改。首先，您需要创建一个 [create a new branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) 来处理您的更改：

```bash
git checkout -b changes-to-docs
```

Now, go ahead and edit one of the files under `docs/`, say `docs/tutorial.rst` - change
it however you want. Check out the
[ReStructuredText Primer](http://docutils.sourceforge.net/docs/user/rst/quickstart.html)
for a reference on the formatting of the rst files.

现在，继续编辑 `docs/` 下的一个文件，比如 `docs/tutorial.rst` - 根据需要进行更改。查看 [ReStructuredText Primer](http://docutils.sourceforge.net/docs/user/rst/quickstart.html) 以获取有关 rst 文件格式的参考。

Once you've made your changes, run this command to convert the docs into HTML:

更改后，运行此命令将文档转换为 HTML：

```bash
make html
```

You'll see a lot of output as Sphinx handles the conversion. After it's done, the
HTML Sphinx generated should be in `docs/_build/html`. Navigate there
and start a simple web server so we can check out the docs in a browser:

在 Sphinx 处理转换时，您将看到大量输出。完成之后，Sphinx 生成的 HTML 应该在 `docs/_build/html` 中。导航到此处并启动一个简单的 web 服务器，这样我们就可以在浏览器中查看文档:

```bash
cd docs/_build/html
python -m http.server # Python2 users should use SimpleHTTPServer

```

This will start a small Python web server listening on port 8000. Point your
browser to http://localhost:8000, find the file
you edited earlier, and check out your changes!

这将启动一个监听端口 8000 的小型 Python web 服务器。将浏览器指向 http://localhost:8000，找到您先前编辑的文件，然后检查您的更改！

If you've made a change you'd like to contribute to the actual docs, just commit
your code, push your new branch to Github:

如果你已经做了改变，你想贡献给实际的文档，只要提交你的代码，把你的新分支推到 Github:

```bash
git add docs/tutorial.rst
git commit -m 'Awesome new change to tutorial'
git push origin changes-to-docs
```

然后, [open a pull request](https://help.github.com/articles/about-pull-requests/).

#### Images

图片

If you're adding new images to the documentation, you'll notice that the images
referenced in the rst, e.g.

如果您正在向文档中添加新图片，您将注意到 rst 中引用的图片，例如

    .. image:: _static/images/tutorial/tutorial_01_sources_database.png

aren't actually stored in that directory. Instead, you should add and commit
images (and any other static assets) to the `superset-frontend/images` directory.
When the docs are deployed to https://superset.incubator.apache.org/, images
are copied from there to the `_static/images` directory, just like they're referenced
in the docs.

实际上并没有存储在那个目录中。相反，您应该向 `superset-frontend/images` 目录添加和提交图片(以及任何其他静态资源)。当文档部署到 https://superset.incubator.apache.org/ 时，图片将从那里复制到`_static/images` 目录，就像在文档中引用它们一样。

For example, the image referenced above actually lives in `superset-frontend/images/tutorial`. Since the image is moved during the documentation build process, the docs reference the image in `_static/images/tutorial` instead.

例如，上面引用的图像实际上位于 `superset-frontend/images/tutorial`中。由于图像是在文档构建过程中移动的，所以文档在 `_static/images/tutorial` 中引用图像。

#### API documentation

API 文档

Generate the API documentation with:

使用以下工具生成 API 文档:

```bash
pip install -r docs/requirements.txt
python setup.py build_sphinx
```

### Flask server

Flask 服务器

#### OS Dependencies

系统依赖

Make sure your machine meets the [OS dependencies](https://superset.incubator.apache.org/installation.html#os-dependencies) before following these steps.

在执行这些步骤之前，请确保您的机器符合[操作系统依赖项](https://superset.incubator.apache.org/installation.html#os-dependencies)。

Developers should use a virtualenv.

开发人员应该使用 virtualenv。

```
pip install virtualenv
```

Then proceed with:

然后继续

```bash
# Create a virtual environemnt and activate it (recommended)
# 创建并激活虚拟环境（推荐）
virtualenv -p python3 venv # setup a python3.6 virtualenv 设置 python3.6 virtualenv
source venv/bin/activate

# Install external dependencies
# 安装外部依赖项
pip install -r requirements.txt
pip install -r requirements-dev.txt

# Install Superset in editable (development) mode
# 在可编辑（开发）模式下安装 Superset
pip install -e .

# Create an admin user in your metadata database
# 在元数据数据库中创建一个管理用户
superset fab create-admin

# Initialize the database
# 初始化数据库
superset db upgrade

# Create default roles and permissions
# 创建默认角色和权限
superset init

# Load some data to play with
# 加载一些数据来处理
superset load_examples

# Start the Flask dev web server from inside your virtualenv.
# Note that your page may not have css at this point.
# See instructions below how to build the front-end assets.
# 从 virtualenv 中启动 Flask dev web 服务器。
# 请注意，您的页面此时可能没有 css。
# 参见下面关于如何构建前端资源的说明。
FLASK_ENV=development superset run -p 8088 --with-threads --reload --debugger
```

**Note: the FLASK_APP env var should not need to be set, as it's currently controlled
via `.flaskenv`, however if needed, it should be set to `superset.app:create_app()`**

**Note: 不需要设置 FLASK_APP 环境变量，因为它目前是通过 `.flaskenv` 控制的，但是如果需要，它应该通过 `superset.app:create_app()`被设置**

If you have made changes to the FAB-managed templates, which are not built the same way as the newer, React-powered front-end assets, you need to start the app without the `--with-threads` argument like so:
`FLASK_ENV=development superset run -p 8088 --reload --debugger`

如果您对 FAB 管理的模板进行了更改，而这些模板的构建方式与较新的、React 驱动的前端资源不同，那么您需要在启动应用程序时不使用 `--with-threads`参数，如下所示：
`FLASK_ENV=development superset run -p 8088 --reload --debugger`

#### Logging to the browser console

输出日志到浏览器控制台

This feature is only available on Python 3. When debugging your application, you can have the server logs sent directly to the browser console using the [ConsoleLog](https://github.com/betodealmeida/consolelog) package. You need to mutate the app, by adding the following to your `config.py` or `superset_config.py`:

此功能仅在 Python3 上可用。调试应用程序时，可以使用 [ConsoleLog](https://github.com/betodealmeida/consolelog) 包将服务器日志直接发送到浏览器控制台。您需要修改应用程序，将以下内容添加到您的 `config.py` 或 `superset_config.py`：

```python
from console_log import ConsoleLog

def FLASK_APP_MUTATOR(app):
    app.wsgi_app = ConsoleLog(app.wsgi_app, app.logger)
```

Then make sure you run your WSGI server using the right worker type:

然后确保您使用正确的 worker 类型运行您的 WSGI 服务器:

```bash
FLASK_ENV=development gunicorn "superset.app:create_app()" -k "geventwebsocket.gunicorn.workers.GeventWebSocketWorker" -b 127.0.0.1:8088 --reload
```

You can log anything to the browser console, including objects:

你可以 log 任何东西到浏览器控制台，包括对象:

```python
from superset import app
app.logger.error('An exception occurred!')
app.logger.info(form_data)
```

### Frontend Assets

前端资源

Frontend assets (TypeScript, JavaScript, CSS, and images) must be compiled in order to properly display the web UI. The `superset-frontend` directory contains all NPM-managed front end assets. Note that there are additional frontend assets bundled with Flask-Appbuilder (e.g. jQuery and bootstrap); these are not managed by NPM, and may be phased out in the future.

必须编译前端资产(TypeScript、JavaScript、CSS 和图像)才能正确显示 web UI。`superset-frontend` 目录包含所有 npm 管理的前端资源。请注意，有额外的前端资源捆绑 Flask-Appbuilder (如 jQuery 和 bootstrap );这些不是由 NPM 管理的，将来可能会逐步淘汰。

#### nvm and node

nvm 和 node

First, be sure you are using recent versions of NodeJS and npm. Using [nvm](https://github.com/creationix/nvm) to manage them is recommended. Check the docs at the link to be sure, but at the time of writing the following would install nvm and node:

首先，确保您使用的是最新版本的 NodeJS 和 npm。建议使用 [nvm](https://github.com/creationix/nvm) 来管理它们。请查看链接中的文档以确定，但在撰写本文时，下面将安装 nvm 和 node:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
nvm install node
```

#### Prerequisite

前提条件

#### Installing Dependencies

安装依赖项

Install third-party dependencies listed in `package.json`:

安装 `package.json` 中列出的第三方依赖项：

```bash
# From the root of the repository
# 从仓库的根目录中
cd superset-frontend

# Install dependencies from `package-lock.json`
# 从 `package-lock.json` 安装依赖项
npm ci
```

#### Building

构建

You can run the Webpack dev server (in a separate terminal from Flask), which runs on port 9000 and proxies non-asset requests to the Flask server on port 8088. After pointing your browser to `http://localhost:9000`, updates to asset sources will be reflected in-browser without a refresh.

您可以运行 Webpack dev server(在与 Flask 分开的一个终端中)，它运行在端口 9000 上，并将非资源请求代理到端口 8088 上的 Flask 服务器。将浏览器指向 `http://localhost:9000` 后，对 asset 源的更新将在浏览器中反映出来，而不需要刷新。

```bash
# Run the dev server
# 运行 dev server
npm run dev-server

# Run the dev server on a non-default port
# 在非默认端口上运行 dev server
npm run dev-server -- --devserverPort=9001

# Run the dev server proxying to a Flask server on a non-default port
# 在非默认端口上运行代理到 Flask server 的 dev server
npm run dev-server -- --supersetPort=8081
```

Alternatively you can use one of the following commands.

或者，可以使用以下命令之一。

```bash
# Start a watcher that recompiles your assets as you modify them (but have to manually reload your browser to see changes.)
# 启动一个监视程序，在您修改资源时重新编译它们(但是必须手动重新加载浏览器才能看到更改)。
npm run dev

# Compile the TypeScript/JavaScript and CSS in production/optimized mode for official releases
# 以 production/optimized 模式为正式发布编译 TypeScript/JavaScript 和 CSS
npm run prod
```

If you run this service from somewhere other than your local machine, you may need to add hostname value to webpack.config.js at .devServer.public specifying the endpoint at which you will access the app. For example: myhost:9001. For convenience you may want to install webpack, webpack-cli and webpack-dev-server globally so that you can run them directly:

如果您在本地机器之外的其他地方运行此服务，您可能需要在 .devServer.public 处向 webpack.config.js 添加 hostname 值，指定您将访问 app 的端点，例如 :myhost:9001。为了方便，你可能想要在全局范围内安装 webpack, webpack-cli 和 webpack-dev-server，这样你就可以直接运行它们:

```bash
npm install --global webpack webpack-cli webpack-dev-server
```

#### Docker (docker-compose)

See docs [here](docker/README.md)

查看文档，[这里](docker/README.md)

#### Updating NPM packages

更新 NPM 包

Use npm in the prescribed way, making sure that
`superset-frontend/package-lock.json` is updated according to `npm`-prescribed
best practices.

按照规定的方式使用 npm，确保 `superset-frontend/package-lock.json` 是根据`npm`-prescribed 的最佳实践更新。

#### Feature flags

功能标记

Superset supports a server-wide feature flag system, which eases the incremental development of features. To add a new feature flag, simply modify `superset_config.py` with something like the following:

Superset 支持服务器范围的功能标记系统，这有助于特性的增量开发。要添加新的功能标记，只需使用如下内容修改 `superset_config.py`：

```python
FEATURE_FLAGS = {
    'SCOPED_FILTER': True,
}
```

If you want to use the same flag in the client code, also add it to the FeatureFlag TypeScript enum in `superset-frontend/src/featureFlags.ts`. For example,

如果你想在客户端代码中使用相同的标记，也可以将它添加到 `superset-frontend/src/featureFlags.ts` 中的 FeatureFlag TypeScript enum 中。例如,

```typescript
export enum FeatureFlag {
  SCOPED_FILTER = 'SCOPED_FILTER',
}
```

`superset/config.py` contains `DEFAULT_FEATURE_FLAGS` which will be overwritten by
those specified under FEATURE_FLAGS in `superset_config.py`. For example, `DEFAULT_FEATURE_FLAGS = { 'FOO': True, 'BAR': False }` in `superset/config.py` and `FEATURE_FLAGS = { 'BAR': True, 'BAZ': True }` in `superset_config.py` will result
in combined feature flags of `{ 'FOO': True, 'BAR': True, 'BAZ': True }`.

`superset/config.py` 包含 `DEFAULT_FEATURE_FLAGS`，它将被 `superset_config.py` 中的 FEATURE_FLAGS 中指定的那些覆盖。例如：
`DEFAULT_FEATURE_FLAGS = { 'FOO': True, 'BAR': False }` 在 `superset/config.py` 中， `FEATURE_FLAGS = { 'BAR': True, 'BAZ': True }` 在 `superset_config.py` 中。合并后的功能标记是 `{ 'FOO': True, 'BAR': True, 'BAZ': True }`。

## Git Hooks

Superset uses Git pre-commit hooks courtesy of [pre-commit](https://pre-commit.com/). To install run the following:

Superset 使用 Git pre-commit 钩子，由 [pre-commit](https://pre-commit.com/) 提供。要安装，请运行以下命令：

```bash
pip3 install -r requirements-dev.txt
pre-commit install
```

## Linting

Lint 这个项目使用：

```bash
# 针对 python
tox -e flake8

# 针对 frontend
cd superset-frontend
npm ci
npm run lint
```

The Python code is auto-formatted using [Black](https://github.com/python/black) which
is configured as a pre-commit hook. There are also numerous [editor integrations](https://black.readthedocs.io/en/stable/editor_integration.html).

Python 代码是使用 [Black](https://github.com/python/black) 自动格式化，它被配置在 pre-commit hook 中。还有许多 [编辑器集成](https://black.readthedocs.io/en/stable/editor_integration.html)。

## Conventions

约定

### Python

Parameters in the `config.py` (which are accessible via the Flask app.config dictionary) are assummed to always be defined and thus should be accessed directly via,

`config.py` 中的参数(可以通过 Flask app.config 字典访问)假设总是被定义，因此应该通过以下方式直接访问:

```python
blueprints = app.config["BLUEPRINTS"]
```

rather than,

而不是，

```python
blueprints = app.config.get("BLUEPRINTS")
```

or similar as the later will cause typing issues. The former is of type `List[Callable]` whereas the later is of type `Optional[List[Callable]]`.

或类似的，后者将导致 typing issues。前者的类型是 `List[Callable]`，而后者的类型是 `Optional[List[Callable]]`。

## Typing

### Python

To ensure clarity, consistency, all readability, _all_ new functions should use
[type hints](https://docs.python.org/3/library/typing.html) and include a
docstring using Sphinx documentation.

为了确保清晰、一致性和可读性，_所有_ 新函数都应该使用 [type hints](https://docs.python.org/3/library/typing.html)，并使用 Sphinx 文档包含 docstring。

Note per [PEP-484](https://www.python.org/dev/peps/pep-0484/#exceptions) no
syntax for listing explicitly raised exceptions is proposed and thus the
recommendation is to put this information in a docstring, i.e.,

请注意，根据 [PEP-484](https://www.python.org/dev/peps/pep-0484/#exceptions)，不建议使用任何语法来列出显式引发的异常，因此建议将这些信息放在 docstring 中，即，

```python
import math
from typing import Union


def sqrt(x: Union[float, int]) -> Union[float, int]:
    """
    Return the square root of x.

    :param x: A number
    :returns: The square root of the given number
    :raises ValueError: If the number is negative
    """

    """
    返回 x 的平方根。

    :param x: 一个数字
    :returns: 给定数字的平方根
    :raises ValueError: 如果数字是负数
    """

    return math.sqrt(x)
```

### TypeScript

TypeScript is fully supported and is the recommended language for writing all new frontend components. When modifying existing functions/components, migrating to TypeScript is appreciated, but not required. Examples of migrating functions/components to TypeScript can be found in [#9162](https://github.com/apache/incubator-superset/pull/9162) and [#9180](https://github.com/apache/incubator-superset/pull/9180).

TypeScript 是完全支持的，是编写所有新的前端组件的推荐语言。当修改现有的 functions/components 时，可以迁移到 TypeScript，但不是必需的。将 functions/components 迁移到TypeScript 的例子可以在 [#9162](https://github.com/apache/incubator-superset/pull/9162) 和 [#9180](https://github.com/apache/incubator-superset/pull/9180) 中找到。

## Testing

测试

### Python Testing

Python 测试

All python tests are carried out in [tox](https://tox.readthedocs.io/en/latest/index.html)
a standardized testing framework.
All python tests can be run with any of the tox [environments](https://tox.readthedocs.io/en/latest/example/basic.html#a-simple-tox-ini-default-environments), via,

所有的 python 测试都在 [tox](https://tox.readthedocs.io/en/latest/index.html) 标准测试框架中进行。所有的 python 测试都可以在任何 tox [environments](https://tox.readthedocs.io/en/latest/example/basic.html#a-simple-tox-ini-default-environments) 下运行，通过，

```bash
tox -e <environment>
```

For example,

例如：

```bash
tox -e py36
```

Alternatively, you can run all tests in a single file via,

或者，您可以通过以下方式在单个文件中运行所有测试:

```bash
tox -e <environment> -- tests/test_file.py
```

or for a specific test via,

或者对于一个特定的测试，

```bash
tox -e <environment> -- tests/test_file.py:TestClassName.test_method_name
```

Note that the test environment uses a temporary directory for defining the
SQLite databases which will be cleared each time before the group of test
commands are invoked.

请注意，测试环境使用一个临时目录来定义 SQLite 数据库，在每次调用测试命令组之前，SQLite 数据库都会被清除。

### Frontend Testing

前端测试

We use [Jest](https://jestjs.io/) and [Enzyme](https://airbnb.io/enzyme/) to test TypeScript/JavaScript. Tests can be run with:

我们使用 [Jest](https://jestjs.io/) 和 [Enzyme](https://airbnb.io/enzyme/) 来测试 TypeScript/JavaScript。测试运行，使用:

```bash
cd superset-frontend
npm run test
```

### Integration Testing

集成测试

We use [Cypress](https://www.cypress.io/) for integration tests. Tests can be run by `tox -e cypress`. To open Cypress and explore tests first setup and run test server:

我们使用 [Cypress](https://www.cypress.io/) 进行集成测试。测试通过 `tox -e cypress` 运行。要打开 Cypress 并探索测试，首先要设置和运行测试服务器：

```bash
export SUPERSET_CONFIG=tests.superset_test_config
superset db upgrade
superset init
superset load_test_users
superset load_examples
superset run --port 8081
```

Run Cypress tests:

运行 Cypress 测试：

```bash
cd superset-frontend
npm run build

cd cypress-base
npm install
npm run cypress run

# run tests from a specific file
# 从指定文件运行测试
npm run cypress run -- --spec cypress/integration/explore/link.test.js

# run specific file with video capture
# 运行特定的文件使用视频捕获
npm run cypress run -- --spec cypress/integration/dashboard/index.test.js --config video=true

# to open the cypress ui
# 打开 cypress ui
npm run cypress open
```

查看 [`superset-frontend/cypress_build.sh`](https://github.com/apache/incubator-superset/blob/master/superset-frontend/cypress_build.sh).

## Translating

翻译

We use [Babel](http://babel.pocoo.org/en/latest/) to translate Superset.
In Python files, we import the magic `_` function using:

我们用 [Babel](http://babel.pocoo.org/en/latest/) 来翻译 Superset。在 Python 文件中，我们导入魔术方法 `_`，使用如下：

```python
from flask_babel import lazy_gettext as _
```

then wrap our translatable strings with it, e.g. `_('Translate me')`.
During extraction, string literals passed to `_` will be added to the
generated `.po` file for each language for later translation.

然后用它来包装我们的可翻译字符串，例如：`_('Translate me')`。提取过程中，传递给 `_` 的字面量将被添加到为每种语言生成的 `.po` 文件中，以供以后翻译。

At runtime, the `_` function will return the translation of the given
string for the current language, or the given string itself
if no translation is available.

在运行时，`_` 函数将返回当前语言的给定字符串的翻译，如果没有可用的翻译，则返回给定字符串本身。

In TypeScript/JavaScript, the technique is similar:
we import `t` (simple translation), `tn` (translation containing a number).

在 TypeScript/JavaScript 中，技术是类似的: 我们导入 `t` (简单翻译)，`tn` (包含数字的翻译)。

```javascript
import { t, tn } from "@superset-ui/translation";
```

### Enabling language selection

启用多语言

Add the `LANGUAGES` variable to your `superset_config.py`. Having more than one
option inside will add a language selection dropdown to the UI on the right side
of the navigation bar.

将 `LANGUAGES` 变量添加到您的 `superset_config.py` 中。如果其中有多个选项，则会在导航栏右侧的 UI 中添加一个语言选择下拉菜单。

```python
LANGUAGES = {
    'en': {'flag': 'us', 'name': 'English'},
    'fr': {'flag': 'fr', 'name': 'French'},
    'zh': {'flag': 'cn', 'name': 'Chinese'},
}
```

### Extracting new strings for translation

提取新的字符串进行翻译

```bash
flask fab babel-extract --target superset/translations --output superset/translations/messages.pot --config superset/translations/babel.cfg -k _ -k __ -k t -k tn -k tct
```

You can then translate the strings gathered in files located under
`superset/translation`, where there's one per language. You can use [Poedit](https://poedit.net/features)
to translate the `po` file more conveniently.
There are some [tutorials in the wiki](https://wiki.lxde.org/en/Translate_*.po_files_with_Poedit).

然后可以翻译 `superset/translation` 文件夹下收集的字符串，其中每种语言都有一个。您可以使用 [Poedit](https://poedit.net/features) 更方便地翻译 `po` 文件。wiki 中有一些[教程](https://wiki.lxde.org/en/Translate_*.po_files_with_Poedit)。

For the translations to take effect:

为使译文生效:

```bash
# In the case of JS translation, we need to convert the PO file into a JSON file, and we need the global download of the npm package po2json.
# 在 JS 转换的情况下，我们需要将 PO 文件转换成 JSON 文件，我们需要全局下载 po2json 的npm 包。
npm install -g po2json
flask fab babel-compile --target superset/translations
# Convert the en PO file into a JSON file
# 将 en PO 文件转换为 JSON 文件
po2json -d superset -f jed1.x superset/translations/en/LC_MESSAGES/messages.po superset/translations/en/LC_MESSAGES/messages.json
```

If you get errors running `po2json`, you might be running the Ubuntu package with the same
name, rather than the NodeJS package (they have a different format for the arguments). If
there is a conflict, you may need to update your `PATH` environment variable or fully qualify
the executable path (e.g. `/usr/local/bin/po2json` instead of `po2json`).
If you get a lot of `[null,***]` in `messages.json`, just delete all the `null,`.
For example, `"year":["年"]` is correct while `"year":[null,"年"]`is incorrect.

如果您在运行 `po2json` 时出现错误，那么您可能正在运行同名的 Ubuntu 包，而不是 NodeJS 包(它们的参数格式不同)。如果存在冲突，您可能需要更新 `PATH` 环境变量或完全限定可执行路径（例如：`/usr/local/bin/po2json` 代替 `po2json`）。如果你在 `messages.json` 得到许多 `[null,***]`，只需要删除所有的 `null,`。例如, `"year":["年"]` 是正确的,而 `"year":[null,"年"]` 是不正确的。

### Creating a new language dictionary

创建一个新的语言字典

To create a dictionary for a new language, run the following, where `LANGUAGE_CODE` is replaced with
the language code for your target language, e.g. `es` (see [Flask AppBuilder i18n documentation](https://flask-appbuilder.readthedocs.io/en/latest/i18n.html) for more details):

要为一种新语言创建字典，运行以下命令，其中 `LANGUAGE_CODE` 将被替换为目标语言的语言代码，例如（查看 [Flask AppBuilder i18n documentation](https://flask-appbuilder.readthedocs.io/en/latest/i18n.html) 了解更多信息 ）：

```bash
pip install -r superset/translations/requirements.txt
pybabel init -i superset/translations/messages.pot -d superset/translations -l LANGUAGE_CODE
```

Then, [extract strings for the new language](#extracting-new-strings-for-translation).

然后，[extract strings for the new language](#extracting-new-strings-for-translation)

## Tips

提示

### Adding a new datasource

添加一个新的数据源

1. Create Models and Views for the datasource, add them under superset folder, like a new my_models.py
   with models for cluster, datasources, columns and metrics and my_views.py with clustermodelview
   and datasourcemodelview.

1. 创建数据源的模型和视图，将它们添加到 superset 文件夹下，如新建 my_models.py，其中包含用于集群、数据源、列和指标的模型，以及 my_views.py，其中包含 clustermodelview 和datasourcemodelview。

1. Create DB migration files for the new models

1. 为新模型创建 DB 迁移文件

1. Specify this variable to add the datasource model and from which module it is from in config.py:

1. 指定这个变量来添加 datasource 模型，以及它来自 config.py 中的哪个模块:

   例如:

   ```python
   ADDITIONAL_MODULE_DS_MAP = {'superset.my_models': ['MyDatasource', 'MyOtherDatasource']}
   ```

   This means it'll register MyDatasource and MyOtherDatasource in superset.my_models module in the source registry.

   这意味着它将在源注册表的 superset.my_models 模块中注册 MyDatasource 和 MyOtherDatasource。

### Creating a new visualization type

创建一个新的可视化类型

Here's an example as a Github PR with comments that describe what the
different sections of the code do:
https://github.com/apache/incubator-superset/pull/3013

下面是一个 Github PR 示例，其中包含描述代码不同部分的注释：
https://github.com/apache/incubator-superset/pull/3013

### Adding a DB migration

添加数据库迁移

1. Alter the model you want to change. This example will add a `Column` Annotations model.

1. 改变你想要改变的模型。本例将添加一个 `Column` 注释模型。

   [Example commit](https://github.com/apache/incubator-superset/commit/6c25f549384d7c2fc288451222e50493a7b14104)

1. Generate the migration file

1. 生成迁移文件

   ```bash
   superset db migrate -m 'add_metadata_column_to_annotation_model.py'
   ```

   这将生成一个文件 `migrations/version/{SHA}_this_will_be_in_the_migration_filename.py`.

   [Example commit](https://github.com/apache/incubator-superset/commit/d3e83b0fd572c9d6c1297543d415a332858e262)

1. Upgrade the DB

1. 升级数据库

   ```bash
   superset db upgrade
   ```

   The output should look like this:

   ```
   INFO  [alembic.runtime.migration] Context impl SQLiteImpl.
   INFO  [alembic.runtime.migration] Will assume transactional DDL.
   INFO  [alembic.runtime.migration] Running upgrade 1a1d627ebd8e -> 40a0a483dd12, add_metadata_column_to_annotation_model.py
   ```

1. Add column to view

1. 添加列到视图

   Since there is a new column, we need to add it to the AppBuilder Model view.

   由于有一个新列，我们需要将它添加到 AppBuilder 模型视图中。

   [Example commit](https://github.com/apache/incubator-superset/pull/5745/commits/6220966e2a0a0cf3e6d87925491f8920fe8a3458)

1. Test the migration's `down` method

1. 测试迁移的 `down` 方法

   ```bash
   superset db downgrade
   ```

   The output should look like this:

   输出应该是这样的：

   ```
   INFO  [alembic.runtime.migration] Context impl SQLiteImpl.
   INFO  [alembic.runtime.migration] Will assume transactional DDL.
   INFO  [alembic.runtime.migration] Running downgrade 40a0a483dd12 -> 1a1d627ebd8e, add_metadata_column_to_annotation_model.py
   ```

### Merging DB migrations

合并DB迁移

When two DB migrations collide, you'll get an error message like this one:

当两个DB迁移发生冲突时，您将得到类似这样的错误消息：

```
alembic.util.exc.CommandError: Multiple head revisions are present for
given argument 'head'; please specify a specific target
revision, '<branchname>@head' to narrow to a specific head,
or 'heads' for all heads`
```

To fix it:

修复:

1. Get the migration heads

1. 得到迁移头

   ```bash
   superset db heads
   ```

   This should list two or more migration hashes.

   这应该列出两个或更多的迁移散列。

1. Create a new merge migration

1. 创建一个新的合并迁移

   ```bash
   superset db merge {HASH1} {HASH2}
   ```

1. Upgrade the DB to the new checkpoint

1. 将数据库升级到新的检查点

   ```bash
   superset db upgrade
   ```

### SQL Lab Async

SQL Lab 异步

It's possible to configure a local database to operate in `async` mode,
to work on `async` related features.

可以将本地数据库配置为在 `async` 模式下操作，以处理 `async` 相关功能。

To do this, you'll need to:

为此，您需要：

- Add an additional database entry. We recommend you copy the connection
  string from the database labeled `main`, and then enable `SQL Lab` and the
  features you want to use. Don't forget to check the `Async` box
- 添加一个额外的数据库条目。我们建议您从标记为 `main` 的数据库中复制连接字符串，然后启用`SQL Lab` 和您想要使用的功能。不要忘记勾选 `Async` 框
- Configure a results backend, here's a local `FileSystemCache` example,
  not recommended for production,
  but perfect for testing (stores cache in `/tmp`)
  ```python
  from werkzeug.contrib.cache import FileSystemCache
  RESULTS_BACKEND = FileSystemCache('/tmp/sqllab')
  ```
- 配置一个结果后端，这是一个本地 `FileSystemCache` 示例，不建议用于生产，但非常适合
  用于测试(将缓存存储在 `/tmp` 中)
  ```python
  from werkzeug.contrib.cache import FileSystemCache
  RESULTS_BACKEND = FileSystemCache('/tmp/sqllab')
  ```


* 启动一个 celery worker
  ```shell script
  celery worker --app=superset.tasks.celery_app:app -Ofair
  ```

Note that:

请注意：

- for changes that affect the worker logic, you'll have to
  restart the `celery worker` process for the changes to be reflected.
- 对于影响 worker 逻辑的更改，您必须重新启动 `celery worker` 进程，以反映更改。
- The message queue used is a `sqlite` database using the `SQLAlchemy`
  experimental broker. Ok for testing, but not recommended in production
- 使用的消息队列是一个 `sqlite` 数据库，使用的是 `SQLAlchemy` 实验代理。用于测试是可以的，但不建议用于生产
- In some cases, you may want to create a context that is more aligned
  to your production environment, and use the similar broker as well as
  results backend configuration
- 在某些情况下，您可能希望创建与生产环境更一致的上下文，并使用类似的代理和结果后端配置

## Chart Parameters

图表参数

Chart parameters are stored as a JSON encoded string the `slices.params` column and are often referenced throughout the code as form-data. Currently the form-data is neither versioned nor typed as thus is somewhat free-formed. Note in the future there may be merit in using something like [JSON Schema](https://json-schema.org/) to both annotate and validate the JSON object in addition to using a Mypy `TypedDict` (introduced in Python 3.8) for typing the form-data in the backend. This section serves as a potential primer for that work.

图表参数以 JSON 编码的字符串存储在 `slices.params` 列，在整个代码中经常作为表单数据引用。目前，表单数据既没有版本控制，也没有类型化，因此在某种程度上是自由格式的。注意: 将来除了使用 Mypy `TypedDict` (在 Python 3.8 中引入)在后端键入表单数据之外，还可以使用类似 JSON 模式的东西来注释和验证 JSON 对象，这可能是有价值的。本节将作为该工作的潜在入门。

The following tables provide a non-exhausive list of the various fields which can be present in the JSON object grouped by the Explorer pane sections. These values were obtained by extracting the distinct fields from a legacy deployment consisting of tens of thousands of charts and thus some fields may be missing whilst others may be deprecated.

下表提供了一个不详细的字段列表，这些字段可以出现在按 Explorer 窗格节分组的JSON对象中。这些值是通过从由成千上万个图表组成的遗留部署中提取不同的字段获得的，因此一些字段可能会丢失，而另一些可能会被弃用。

Note not all fields are correctly catagorized. The fields vary based on visualization type and may apprear in different sections depending on the type. Verified deprecated columns may indicate a missing migration and/or prior migrations which were unsucessful and thus future work may be required to clean up the form-data.

注意，并不是所有字段都被正确分解了。字段根据可视化类型不同而有所不同，并且可能根据类型在不同的部分中理解。已验证的废弃列可能表明缺少迁移和/或以前的迁移不成功，因此可能需要进行后续工作来清理表单数据。

### Datasource & Chart Type

| Field             | Type     | Notes                               |
| ----------------- | -------- | ----------------------------------- |
| `database_name`   | _string_ | _Deprecated?_                       |
| `datasource`      | _string_ | `<datasouce_id>__<datasource_type>` |
| `datasource_id`   | _string_ | _Deprecated?_ See `datasource`      |
| `datasource_name` | _string_ | _Deprecated?_                       |
| `datasource_type` | _string_ | _Deprecated?_ See `datasource`      |
| `viz_type`        | _string_ | The **Visualization Type** widget   |

### Time

| Field                  | Type            | Notes                                 |
| ---------------------- | --------------- | ------------------------------------- |
| `date_filter`          | _N/A_           | _Deprecated?_                         |
| `date_time_format`     | _N/A_           | _Deprecated?_                         |
| `druid_time_origin`    | _string_        | The Druid **Origin** widget           |
| `granularity`          | _string_        | The Druid **Time Granularity** widget |
| `granularity_sqla`     | _string_        | The SQLA **Time Column** widget       |
| `time_grain_sqla`      | _string_        | The SQLA **Time Grain** widget        |
| `time_range`           | _string_        | The **Time range** widget             |
| `time_range_endpoints` | _array(string)_ | Used by SIP-15 [HIDDEN]               |

### GROUP BY

| Field                     | Type            | Notes                       |
| ------------------------- | --------------- | --------------------------- |
| `include_time`            | _boolean_       | The **Include Time** widget |
| `metrics`                 | _array(string)_ | See Query section           |
| `order_asc`               | -               | See Query section           |
| `percent_metrics`         | -               | See Query section           |
| `row_limit`               | -               | See Query section           |
| `timeseries_limit_metric` | -               | See Query section           |

### NOT GROUPED BY

| Field           | Type            | Notes                   |
| --------------- | --------------- | ----------------------- |
| `all_columns`   | _array(string)_ | The **Columns** widget  |
| `order_by_cols` | _array(string)_ | The **Ordering** widget |
| `row_limit`     | -               | See Query section       |

### Y Axis 1

| Field           | Type | Notes                                              |
| --------------- | ---- | -------------------------------------------------- |
| `metric`        | -    | The **Left Axis Metric** widget. See Query section |
| `y_axis_format` | -    | See Y Axis section                                 |

### Y Axis 2

| Field             | Type     | Notes                                               |
| ----------------- | -------- | --------------------------------------------------- |
| `metric_2`        | -        | The **Right Axis Metric** widget. See Query section |
| `y_axis_2_format` | _string_ | The **Right Axis Format** widget                    |

### Query

| Field                                                                                                  | Type                                              | Notes                                             |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------- | ------------------------------------------------- |
| `adhoc_filters`                                                                                        | _array(object)_                                   | The **Filters** widget                            |
| `all_columns_x`                                                                                        | _array(string)_                                   | The **Numeric Columns** widget                    |
| `columns`                                                                                              | _array(string)_                                   | The **Breakdowns** widget                         |
| `contribution`                                                                                         | _boolean_                                         | The **Contribution** widget                       |
| `groupby`                                                                                              | _array(string)_                                   | The **Group by** or **Series** widget             |
| `limit`                                                                                                | _number_                                          | The **Series Limit** widget                       |
| `max_bubble_size`                                                                                      | _number_                                          | The **Max Bubble Size** widget                    |
| `metric`<br>`metric_2`<br>`metrics`<br>`percent_mertics`<br>`secondary_metric`<br>`size`<br>`x`<br>`y` | _string_,_object_,_array(string)_,_array(object)_ | The metric(s) depending on the visualization type |
| `order_asc`                                                                                            | _boolean_                                         | The **Sort Descending** widget                    |
| `row_limit`                                                                                            | _number_                                          | The **Row limit** widget                          |
| `timeseries_limit_metric`                                                                              | _object_                                          | The **Sort By** widget                            |

The `metric` (or equivalent) and `timeseries_limit_metric` fields are all composed of either metric names or the JSON representation of the `AdhocMetric` TypeScript type. The `adhoc_filters` is composed of the JSON represent of the `AdhocFilter` TypeScript type (which can comprise of columns or metrics depending on whether it is a WHERE or HAVING clause). The `all_columns`, `all_columns_x`, `columns`, `groupby`, and `order_by_cols` fields all represent column names.

`metric` (or equivalent) 和 `timeseries_limit_metric` 字段都是由度量名称或者 `AdhocMetric` TypeScript类型的JSON 表示形式组成的。`adhoc_filters` 由表示 `AdhocFilter` TypeScript 类型的 JSON 组成(可以由列或指标组成，这取决于它是 WHERE 子句还是 HAVING 子句)。`all_columns`、`all_columns_x`、`columns`、`groupby` 和 `order_by_cols` 字段都表示列名。

### Filters Configuration

| Field            | Type          | Notes                             |
| ---------------- | ------------- | --------------------------------- |
| `filter_configs` | array(object) | The filter-box **Filters** widget |

The filter-box configuration references column names (via the `column` key) and optionally metric names (via the `metric` key) if sorting is defined.

如果定义了排序，那么过滤框配置将引用列名(通过 `column` 键)和可选的度量名称(通过 `metric` 键)。


### Options

| Field                  | Type      | Notes                                |
| ---------------------- | --------- | ------------------------------------ |
| `compare_lag`          | _number_  | The **Comparison Period Lag** widget |
| `compare_suffix`       | _string_  | The **Comparison suffix** widget     |
| `show_trend_line`      | _boolean_ | The **Show Trend Line** widget       |
| `start_y_axis_at_zero` | _boolean_ | The **Start y-axis at 0** widget     |

### Chart Options

| Field                 | Type      | Notes                                            |
| --------------------- | --------- | ------------------------------------------------ |
| `color_picker`        | _object_  | The **Fixed Color** widget                       |
| `donut`               | _boolean_ | The **Donut** widget                             |
| `global_opacity`      | _number_  | The **Opacity** widget                           |
| `header_font_size`    | _number_  | The **Big Number Font Size** widget (or similar) |
| `label_colors`        | _object_  | The **Color Scheme** widget                      |
| `labels_outside`      | _boolean_ | The **Put labels outside** widget                |
| `line_interpolation`  | _string_  | The **Line Style** widget                        |
| `link_length`         | _number_  | The **No of Bins** widget                        |
| `normalized`          | _boolean_ | The **Normalized** widget                        |
| `number_format`       | _string_  | The **Number format** widget                     |
| `pie_label_type`      | _string_  | [HIDDEN]                                         |
| `rich_tooltip`        | _boolean_ | The **Rich Tooltip** widget                      |
| `send_time_range`     | _boolean_ | The **Show Markers** widget                      |
| `show_brush`          | _string_  | The **Show Range Filter** widget                 |
| `show_legend`         | _boolean_ | The **Legend** widget                            |
| `show_markers`        | _string_  | The **Show Markers** widget                      |
| `subheader_font_size` | _number_  | The **Subheader Font Size** widget               |

### X Axis

| Field                | Type      | Notes                        |
| -------------------- | --------- | ---------------------------- |
| `bottom_margin`      | _string_  | The **Bottom Margin** widget |
| `x_axis_format`      | _string_  | The **X Axis Format** widget |
| `x_axis_label`       | _string_  | The **X Axis Label** widget  |
| `x_axis_showminmax`  | _boolean_ | The **X bounds** widget      |
| `x_axis_time_format` | _N/A_     | _Deprecated?_                |
| `x_log_scale`        | _N/A_     | _Deprecated?_                |
| `x_ticks_layout`     | _string_  | The **X Tick Layout** widget |

### Y Axis

| Field               | Type            | Notes                        |
| ------------------- | --------------- | ---------------------------- |
| `left_margin`       | _number_        | The **Left Margin** widget   |
| `y_axis_2_label`    | _N/A_           | _Deprecated?_                |
| `y_axis_bounds`     | _array(string)_ | The **Y Axis Bounds** widget |
| `y_axis_format`     | _string_        | The **Y Axis Format** widget |
| `y_axis_label`      | _string_        | The **Y Axis Label** widget  |
| `y_axis_showminmax` | _boolean_       | The **Y bounds** widget      |
| `y_axis_zero`       | _N/A_           | _Deprecated?_                |
| `y_log_scale`       | _boolean_       | The **Y Log Scale** widget   |
| `yscale_interval`   | _N/A_           | _Deprecated?_                |

Note the `y_axis_format` is defined under various section for some charts.

### Other

| Field          | Type     | Notes        |
| -------------- | -------- | ------------ |
| `color_scheme` | _string_ |              |
| `slice_id`     | _number_ | The slice ID |
| `url_params`   | _object_ |              |

### Unclassified

| Field                           | Type  | Notes |
| ------------------------------- | ----- | ----- |
| `add_to_dash`                   | _N/A_ |       |
| `align_pn`                      | _N/A_ |       |
| `all_columns_y`                 | _N/A_ |       |
| `annotation_layers`             | _N/A_ |       |
| `autozoom`                      | _N/A_ |       |
| `bar_stacked`                   | _N/A_ |       |
| `cache_timeout`                 | _N/A_ |       |
| `canvas_image_rendering`        | _N/A_ |       |
| `cell_padding`                  | _N/A_ |       |
| `cell_radius`                   | _N/A_ |       |
| `cell_size`                     | _N/A_ |       |
| `charge`                        | _N/A_ |       |
| `clustering_radius`             | _N/A_ |       |
| `code`                          | _N/A_ |       |
| `collapsed_fieldsets`           | _N/A_ |       |
| `color_pn`                      | _N/A_ |       |
| `column_collection`             | _N/A_ |       |
| `combine_metric`                | _N/A_ |       |
| `comparison type`               | _N/A_ |       |
| `contribution`                  | _N/A_ |       |
| `country_fieldtype`             | _N/A_ |       |
| `date_filter`                   | _N/A_ |       |
| `deck_slices`                   | _N/A_ |       |
| `default_filters`               | _N/A_ |       |
| `dimension`                     | _N/A_ |       |
| `domain_granularity`            | _N/A_ |       |
| `end_spatial`                   | _N/A_ |       |
| `entity`                        | _N/A_ |       |
| `equal_date_size`               | _N/A_ |       |
| `expanded_slices`               | _N/A_ |       |
| `extra_filters`                 | _N/A_ |       |
| `extruded`                      | _N/A_ |       |
| `fill_color_picker`             | _N/A_ |       |
| `filled`                        | _N/A_ |       |
| `filter_immune_slice_fields`    | _N/A_ |       |
| `filter_immune_slices`          | _N/A_ |       |
| `filter_nulls`                  | _N/A_ |       |
| `flt_col_0`                     | _N/A_ |       |
| `flt_col_1`                     | _N/A_ |       |
| `flt_eq_0`                      | _N/A_ |       |
| `flt_eq_1`                      | _N/A_ |       |
| `flt_op_0`                      | _N/A_ |       |
| `flt_op_1`                      | _N/A_ |       |
| `goto_dash`                     | _N/A_ |       |
| `grid_size`                     | _N/A_ |       |
| `horizon_color_scale`           | _N/A_ |       |
| `import_time`                   | _N/A_ |       |
| `include_search`                | _N/A_ |       |
| `include_series`                | _N/A_ |       |
| `instant_filtering`             | _N/A_ |       |
| `js_agg_function`               | _N/A_ |       |
| `js_columns`                    | _N/A_ |       |
| `label`                         | _N/A_ |       |
| `labels_outside`                | _N/A_ |       |
| `legend_position`               | _N/A_ |       |
| `line_charts`                   | _N/A_ |       |
| `line_charts_2`                 | _N/A_ |       |
| `line_column`                   | _N/A_ |       |
| `line_type`                     | _N/A_ |       |
| `line_width`                    | _N/A_ |       |
| `linear_color_scheme`           | _N/A_ |       |
| `log_scale`                     | _N/A_ |       |
| `mapbox_color`                  | _N/A_ |       |
| `mapbox_label`                  | _N/A_ |       |
| `mapbox_style`                  | _N/A_ |       |
| `marker_labels`                 | _N/A_ |       |
| `marker_line_labels`            | _N/A_ |       |
| `marker_lines`                  | _N/A_ |       |
| `markers`                       | _N/A_ |       |
| `markup_type`                   | _N/A_ |       |
| `max_radius`                    | _N/A_ |       |
| `min_leaf_node_event_count`     | _N/A_ |       |
| `min_periods`                   | _N/A_ |       |
| `min_radius`                    | _N/A_ |       |
| `multiplier`                    | _N/A_ |       |
| `new_dashboard_name`            | _N/A_ |       |
| `new_slice_name`                | _N/A_ |       |
| `normalize_across`              | _N/A_ |       |
| `num_buckets`                   | _N/A_ |       |
| `num_period_compare`            | _N/A_ |       |
| `order_bars`                    | _N/A_ |       |
| `order_by_entity`               | _N/A_ |       |
| `order_desc`                    | _N/A_ |       |
| `page_length`                   | _N/A_ |       |
| `pandas_aggfunc`                | _N/A_ |       |
| `partition_limit`               | _N/A_ |       |
| `partition_threshold`           | _N/A_ |       |
| `period_ratio_type`             | _N/A_ |       |
| `perm`                          | _N/A_ |       |
| `pivot_margins`                 | _N/A_ |       |
| `point_radius`                  | _N/A_ |       |
| `point_radius_fixed`            | _N/A_ |       |
| `point_radius_unit`             | _N/A_ |       |
| `point_unit`                    | _N/A_ |       |
| `prefix_metric_with_slice_name` | _N/A_ |       |
| `range_labels`                  | _N/A_ |       |
| `ranges`                        | _N/A_ |       |
| `rdo_save`                      | _N/A_ |       |
| `reduce_x_ticks`                | _N/A_ |       |
| `refresh_frequency`             | _N/A_ |       |
| `remote_id`                     | _N/A_ |       |
| `render_while_dragging`         | _N/A_ |       |
| `resample_fillmethod`           | _N/A_ |       |
| `resample_how`                  | _N/A_ |       |
| `resample_method`               | _N/A_ |       |
| `resample_rule`                 | _N/A_ |       |
| `reverse_long_lat`              | _N/A_ |       |
| `rolling_periods`               | _N/A_ |       |
| `rolling_type`                  | _N/A_ |       |
| `rose_area_proportion`          | _N/A_ |       |
| `rotation`                      | _N/A_ |       |
| `save_to_dashboard_id`          | _N/A_ |       |
| `schema`                        | _N/A_ |       |
| `select_country`                | _N/A_ |       |
| `series`                        | _N/A_ |       |
| `series_height`                 | _N/A_ |       |
| `show_bar_value`                | _N/A_ |       |
| `show_brush`                    | _N/A_ |       |
| `show_bubbles`                  | _N/A_ |       |
| `show_controls`                 | _N/A_ |       |
| `show_datatable`                | _N/A_ |       |
| `show_druid_time_granularity`   | _N/A_ |       |
| `show_druid_time_origin`        | _N/A_ |       |
| `show_labels`                   | _N/A_ |       |
| `show_metric_name`              | _N/A_ |       |
| `show_perc`                     | _N/A_ |       |
| `show_sqla_time_column`         | _N/A_ |       |
| `show_sqla_time_granularity`    | _N/A_ |       |
| `show_values`                   | _N/A_ |       |
| `size_from`                     | _N/A_ |       |
| `size_to`                       | _N/A_ |       |
| `slice_name`                    | _N/A_ |       |
| `sort_x_axis`                   | _N/A_ |       |
| `sort_y_axis`                   | _N/A_ |       |
| `spatial`                       | _N/A_ |       |
| `stacked_style`                 | _N/A_ |       |
| `start_spatial`                 | _N/A_ |       |
| `steps`                         | _N/A_ |       |
| `stroke_color_picker`           | _N/A_ |       |
| `stroke_width`                  | _N/A_ |       |
| `stroked`                       | _N/A_ |       |
| `subdomain_granularity`         | _N/A_ |       |
| `subheader`                     | _N/A_ |       |
| `table_filter`                  | _N/A_ |       |
| `table_timestamp_format`        | _N/A_ |       |
| `time_compare`                  | _N/A_ |       |
| `time_series_option`            | _N/A_ |       |
| `timed_refresh_immune_slices`   | _N/A_ |       |
| `toggle_polygons`               | _N/A_ |       |
| `transpose_pivot`               | _N/A_ |       |
| `treemap_ratio`                 | _N/A_ |       |
| `url`                           | _N/A_ |       |
| `userid`                        | _N/A_ |       |
| `viewport`                      | _N/A_ |       |
| `viewport_latitude`             | _N/A_ |       |
| `viewport_longitude`            | _N/A_ |       |
| `viewport_zoom`                 | _N/A_ |       |
| `whisker_options`               | _N/A_ |       |
