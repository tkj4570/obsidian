---
title: "我做了一个本地 AI 编程 ROI 复盘系统：AI 编程花掉的 Token，到底换来了什么？"
source: "https://ai.codefather.cn/post/2068743448655155201#heading-0"
author:
  - "[[Ryan]]"
published: 1782-06-20
created: 2026-06-23
description: "我以前只想知道自己 AI 编程花了多少 token。 后来发现，这个数字本身没什么用。 真正的问题是：这些 token 到底换来了什么？ 如果一天用了几千万 token，但我不知道它们是花在功能开发、调试修复、上下文整理，还是无效试错上，那 token 总数只是一个越来越大的数字。它既不能告诉我哪个"
tags:
  - "clippings"
---
我以前只想知道自己 AI 编程花了多少 token。 后来发现，这个数字本身没什么用。 真正的问题是： **这些 token 到底换来了什么？** 如果一天用了几千万 token，但我不知道它们是花在功能开发、调试修复、上下文整理，还是无效试错上，那 token 总数只是一个越来越大的数字。它既不能告诉我哪个项目值得继续投，也不能告诉我下周应该少用重模型，还是该先压缩上下文。 所以我做了 Token Studio。它不是一个普通 token meter，而是一个本地 AI 编程 ROI 复盘系统：先可信地采集本机结构化 token 元数据，再把 token 连接到项目、任务、产出证据、模型策略和行动报告。 Token Studio ROI 是一个本地 AI 编程投入复盘系统：采集 Claude Code、Codex CLI 等工具的结构化 token 元数据，按官方公开价换算成本，并把 token 消耗连接到项目、任务、产出证据、模型策略和行动报告。

项目地址： [GitHub - Token Studio ROI](https://github.com/RyanCoreAI/token-studio-roi) npm registry： [token-studio](https://registry.npmjs.org/token-studio/latest) Release： [v6.0.8](https://github.com/RyanCoreAI/token-studio-roi/releases/tag/v6.0.8) 动图体验： [Token Studio Walkthrough](https://yanxai.com/images/token-studio-roi/token-studio-walkthrough.gif) 原文链接： [token-studio-roi](https://yanxai.com/p/token-studio-roi/) 个人技术博客： [yanxai.com](https://yanxai.com/)

![image.png](https://pic.code-nav.cn/post_picture/1813254542264233985/tB4k89h8Zih8bYO5.webp)

## 1\. 普通 token 看板少回答了一个关键问题

市面上的 token 工具大多能回答“用了多少”。这当然重要，但对高频 AI 编程用户来说还不够。

我真正想回答的是：

- 这些 token 是花在探索、实现、验证、发布，还是重复上下文里？
- 哪些项目消耗最高，最后有没有 PR、commit、文档、部署或可展示产出？
- 重模型是不是被用在了测试验证、上下文整理这种低 ROI 场景？
- 哪些 session 只是在烧 token，却没有形成任何可复盘证据？
- 下周我应该继续用同样的模型策略，还是先把低价值任务切到轻量模型？

这就是 Token Studio 的核心差异：

> 统计工具告诉你用了多少；Token Studio 追问这些 token 换来了什么。

这个定位也影响了整个设计。它不追求做云端 SaaS，不追求团队排行榜，也不为了覆盖数量去伪造 token。它先做一件事：把本地真实 token 变成可信工作证据。

## 2\. Token Studio 的闭环

Token Studio 当前围绕一条闭环设计：

```
真实本地 token
  -> 可信覆盖
  -> 自动证据
  -> ROI 复盘
  -> 模型策略
  -> 行动报告
```

这条链路里，每一步都要回答一个实际问题。

### 2.1 真实本地采集：先确认数据是真的

Token Studio 会读取本机仍然存在、且带有可靠 token 字段的结构化日志。核心可信来源是 Claude Code 和 Codex CLI。

它采集的是结构化使用元数据，例如 source、model、session、timestamp、input/output/cache/reasoning tokens。它不保存 prompt、response、transcript、diff、文件内容或完整本机路径。

这个边界很关键：如果连采集数据本身都不可信，后面的 ROI 判断就只是漂亮图表。

### 2.2 Coverage Trust：解释为什么某些工具没有数据

很多工具会在本机留下目录或日志，但检测到目录不等于拿到了可靠 token。

所以 Token Studio 把来源拆成几类：原生可信采集、ccusage 可导入、实验采集、仅检测到、无可靠 token 字段 / 不支持。

这不是为了保守而保守，而是为了避免一种很危险的假象： **覆盖名单很好看，但实际 token 是估出来的。**

我宁愿页面告诉用户“这个来源现在没有可靠 token 字段”，也不希望它用文本长度估算 token，然后生成看似完整但不能复盘的数据。

### 2.3 Evidence Flywheel：把消耗数字变成工作证据

采到 token 之后，还不够。

真正有价值的是这些 token 对应了什么工作：项目、任务类型、工作目的、阶段、产出状态、产出价值、产出链接，以及这些字段是人工确认、自动推断，还是待确认草稿。

比如一个 session 可以从“某模型消耗了 200 万 token”，变成：

```
项目：Token Studio ROI
任务：功能开发
阶段：实现
产出状态：已完成
产出：commit / PR / 文档
价值：中 / 高
证据来源：自动高置信或人工确认
```

只有走到这一步， `/review` 才能继续判断：哪些 token 有产出，哪些高成本 session 还没归因，哪些模型策略值得调整。

### 2.4 ROI Advisor：不给玄学建议，只给可解释规则

Token Studio 不调用 LLM 生成建议。原因很简单：这个工具本身就是为了帮我少花 token，不应该为了分析 token 再消耗一轮 token。

它用本地规则做判断：

- 高成本未归因 session：先补证据。
- 测试验证、探索、上下文整理使用重模型：建议切到轻量模型。
- 低价值或废弃任务使用高成本模型：建议先轻量试错。
- 高 input / low output：建议压缩上下文。
- cache 复用低且 input 高：建议沉淀项目上下文。
- 未定价模型：不参与美元节省判断。

Savings Simulator 也不声称真实节省金额，只做官方价换算下的策略模拟。

### 2.5 Desktop Pulse：给实时状态一个轻量入口

浏览器里的 Dashboard、Trust、Review 是完整复盘入口。Desktop Pulse 只是伴侣。

它解决的是另一个问题：我不想一直开着浏览器 tab，但想随时知道今天 token 有没有失控。

所以 Pulse 重点展示近 24 小时 token、官方价换算、请求数、输入/输出/cache、模型消耗、来源分布、预算 guardrail 和当前建议。它只读本地 API / SQLite 聚合数据，不上传，也不重新实现采集。

## 3\. 下载和使用全流程

这里给 Windows 用户一段可直接复制运行的完整命令： Power [Shell](https://www.mianshiya.com/bank/1812067519566053377) 版：

```
# 前提：已安装 nvm-windows
nvm install 24.17.0
nvm use 24.17.0

node.exe -v
npm.cmd -v

New-Item -ItemType Directory -Force D:\TokenStudio | Out-Null
Set-Location D:\TokenStudio

$pkg = 'token-studio' + '@' + '6.0.8'
npx.cmd -y $pkg
```

CMD 版：

```
REM 前提：已安装 nvm-windows
nvm install 24.17.0
nvm use 24.17.0

node -v
npm -v

mkdir D:\TokenStudio
cd /d D:\TokenStudio

set pkg=token-studio@6.0.8
npx -y %pkg%
```

如果已经有 Node 24，也可以只运行最后三行。它做的是完整本地真实模式，不是 demo：

```
1. npx 从 npm 下载并运行 token-studio
2. Token Studio 做只读 coverage，检查本机是否有 Claude Code / Codex CLI 结构化 token 日志
3. 通过可信 gate 后，把 event 级 token 元数据写入本地 SQLite
4. 启动 127.0.0.1 上的本地 Web/API 服务
5. 自动打开浏览器 Dashboard
6. 后台定时刷新可信 Claude/Codex token 元数据
7. 在 Trust 页面确认数据可信度
8. 在 Review 页面生成证据队列、模型策略和行动报告
9. 如需实时观察，再打开 Desktop Pulse 或 /live
```

第一次使用可以按这个顺序看：

| 步骤 | 你要做什么 | 页面会告诉你什么 |
| --- | --- | --- |
| 1 | 运行第 3 节固定版本命令 | 下载包、启动本地服务、打开浏览器 |
| 2 | 看 Dashboard | 近周期 token、官方价换算、模型和趋势 |
| 3 | 看 Trust | 当前数据是否是真实 event 级采集，哪些来源可信 |
| 4 | 看 Review | 哪些 token 有证据，哪些 session 需要补归因 |
| 5 | 点生成证据队列 | 把最贵、最值得处理的 session 推到前面 |
| 6 | 导出复盘材料 | 复制复盘证据包、技术博客草稿、简历项目描述 |
| 7 | 开 Desktop Pulse | 实时看 24 小时 token、成本、请求数和模型消耗 |

几个常用命令也可以分开用：

```
$pkg = 'token-studio' + '@' + '6.0.8'

# 真实模式：下载、采集可信 token、启动本地看板
npx -y $pkg

# 只做只读检查，不写 SQLite
npx -y $pkg --dry-run-only --no-open

# 只打开已有本地数据库，不重新采集
npx -y $pkg --no-collect

# 查看本地实时状态摘要
npx -y $pkg statusline --format=text

# 如果你只想看产品界面，可以用合成数据
npx -y $pkg demo
```

注意：第 3 节里的真实模式命令会读取本机结构化 token 元数据，但不会读取 prompt、response、transcript、diff 或完整本机路径。 `demo` 是合成数据，只用于看界面，不代表真实采集成功。

### 3.1 Dashboard：先看成本、模型和趋势

![image.png](https://pic.code-nav.cn/post_picture/1813254542264233985/bMGv0YwDqFU29FXB.webp)

> 这张图回答的问题：当前周期 token、官方价换算、模型消耗和趋势是否异常。

Dashboard 的首屏不应该先解释产品理念，而应该先让用户看到真实数据：总 token、输入、输出、缓存、推理 token、官方价换算、模型分布和趋势。

因为用户打开看板的第一反应通常不是“这个工具有什么功能”，而是：

> 我的 token 到底花在哪里？哪个模型最贵？今天有没有异常？

### 3.2 Trust：确认数据是否能用于复盘

![image.png](https://pic.code-nav.cn/post_picture/1813254542264233985/bYmzmFfDdZEAlapb.webp)

> 这张图回答的问题：当前数据是 demo、旧聚合库，还是可信 event 级真实采集；哪些来源能用于 ROI 判断。

Trust 页面是我认为最容易被低估的一页。

它负责回答：当前是 demo、空库、旧聚合库，还是真实 event 级数据？Claude / Codex / Cursor 等来源分别是什么状态？daily、session、event 之间能不能对齐？哪些来源只是 detected-only，不能当成真实覆盖？

如果这一步不清楚，用户就会把“看起来有数据”误当成“可以做决策”。

### 3.3 Review：把 token 变成 ROI 证据

![image.png](https://pic.code-nav.cn/post_picture/1813254542264233985/P0eMCz7jPrwIdh23.webp)

> 这张图回答的问题：哪些 token 已经有产出证据，哪些 session 仍缺项目、任务、阶段、价值或产出链接。

Review 不是普通报表，而是复盘页。

它关心：哪些 token 产出了东西，哪些高成本 session 仍缺证据，哪些模型策略可以调整，哪些建议应该进入下周行动清单。

我还加了三个专业可复制输出包：

- 复盘证据包
- 技术博客草稿
- 简历 / 面试项目描述

这些内容不是静态 bullet，而是基于当前结构化数据生成的 Markdown，方便直接复制到周报、博客或简历项目说明里。缺人工确认或产出链接时，它会明确写限制，不会编造成果。

### 3.4 Desktop Pulse：桌面实时伴侣

![image.png](https://pic.code-nav.cn/post_picture/1813254542264233985/wkobJQPG6PbPHczS.webp)

> 这张图回答的问题：过去 24 小时 token、成本、请求、缓存复用和模型消耗是否处在可控范围内。

Desktop Pulse 是 v6 的桌面端补强。它不是主产品，也不替代浏览器复盘页。

它更像一个本地实时仪表盘：当我正在高频使用 Claude Code 或 Codex 时，它能快速告诉我今天 token 是否失控、重模型是否用得过多、是否有预算风险、是否该停下来处理 open actions。

### 3.5 动图体验

> 这张动图回答的问题：从 Dashboard 到 Trust、Review、Live，完整复盘流是怎么走的。

动图地址： [https://yanxai.com/images/token-studio-roi/token-studio-walkthrough.gif](https://yanxai.com/images/token-studio-roi/token-studio-walkthrough.gif)

## 4\. 和竞品相比，Token Studio 的差异在哪里

我查过同类项目后，结论比较明确：竞品很强，但强项不一样。

ccusage 的优势是多来源覆盖和 JSON 报表。它能统一读取 Claude Code、Codex、OpenCode、Amp、Goose、Kimi、Qwen、Copilot CLI、Gemini CLI 等本地数据源，并提供 daily、weekly、monthly、session 等视图。

CodeBurn 的优势是 TUI 和快速成本观测，强调按 task、model、project、provider 拆分 AI spend。

TokenTracker 的优势是覆盖工具数量、桌面组件、菜单栏和去重能力。

tokscale 的优势是 CLI/TUI、贡献图、leaderboard 和更强的可视化传播感。

Token Studio 没有选择去硬拼这些方向。它的差异是：

| 维度 | 常见 token 工具 | Token Studio |
| --- | --- | --- |
| 核心问题 | 我用了多少 token | 这些 token 换来了什么 |
| 覆盖策略 | 尽量多源统计 | 可信覆盖 + ccusage bridge，不伪造 token |
| 复盘粒度 | 日期、模型、项目 | 项目、任务、阶段、产出、价值、证据来源 |
| 建议方式 | cost hotspot / tips | 本地规则 ROI Advisor + 行动清单 |
| 输出形态 | 报表或 TUI | 周报、博客、简历项目描述、模型策略 |
| 隐私边界 | 多数本地优先 | 明确不保存正文、diff、完整路径 |

所以它不是 ccusage 的替代品，也不是 CodeBurn 的 TUI 复制品。更准确地说，它是本地复盘层：把可信 token 进一步变成工作证据、策略判断和下周行动。

## 5\. 架构设计

Token Studio 的架构很简单，但每一层都保持边界清楚。

```
Claude Code / Codex CLI 本地日志
        |
        v
结构化 collector
        |
        v
SQLite: token_events / session_usage / daily_usage
        |
        v
Coverage Trust / Reconciliation
        |
        v
Evidence Flywheel
        |
        v
Dashboard / Trust / Review / Live / Desktop Pulse
```

### 5.1 为什么用 SQLite

因为这是个人本地工具。

SQLite 不需要部署数据库，容易备份，适合单用户本地场景，也方便把数据文件明确排除在 npm 包和 Git 仓库之外。

### 5.2 为什么不用云端

AI 编程数据很敏感。即便不保存正文，session、模型、时间、项目名、产出链接也可能透露工作节奏和项目方向。

所以默认选择是：数据留在本地，复盘也在本地完成。

### 5.3 为什么不估算所有工具

覆盖数量本身不是目标。可信覆盖才是目标。

如果某个工具没有稳定 token 字段，Token Studio 不会用文本长度估算 token，也不会把 detected-only 写成采集成功。它会建议用 ccusage bridge 导入结构化 JSON，或者明确标记“当前无可靠 token 字段”。

## 6\. 隐私和安全边界

这部分很重要，但不需要在每一段重复。

Token Studio 的边界集中在几条：

- 不保存 prompt、response、transcript、diff、文件内容或完整本机路径。
- Web API 默认绑定本机地址。
- 普通写接口要求 local Origin + JSON。
- `/api/ingest` 默认关闭，只有设置 `INGEST_TOKEN` 后才启用 Bearer token 写入。
- Desktop Pulse 只读本地聚合数据，不上传，不做远程控制面板。
- 官方价换算不是供应商账单，只用于复盘和策略模拟。

这也是为什么我没有把它做成云端 SaaS。对这个产品来说，隐私不是附加卖点，而是系统边界。

## 7\. 我怎么判断这个项目是否有价值

我不想把 Token Studio 写成“又一个全能平台”。

它解决的是一个很具体的问题：

> 对高频 AI 编程用户来说，token 已经变成持续投入，但缺少一个本地、可信、可复盘的投入产出系统。

如果只看 token 数，意义有限。  
如果 token 能连接到项目、任务、阶段、产出和模型策略，它才开始变成可管理的工作资产。

这个判断也符合软件工程研究里常见的问题-方法-证据-评价结构：先定义真实问题，再做可运行系统，然后用真实数据、限制条件和验收门来评价，而不是只做一个漂亮页面。

Token Studio 不会自动证明“ROI 提升了 37%”。它更保守，也更可信：

- 哪些数据可信。
- 哪些只能看趋势。
- 哪些不能下结论。
- 哪些证据缺口最值得补。
- 哪些模型策略值得下周试。

## 8\. 当前局限

这个项目有明确边界。

第一，它不能恢复所有历史。它只能覆盖本机仍然保留、且日志里有可靠 token 字段的数据。

第二，它不是供应商账单。官方价换算适合做趋势和策略复盘，不适合做财务对账。

第三，它不会读取正文，所以不会自动理解任务质量。产出价值仍然需要人工确认或结构化证据支撑。

第四，它不会为了覆盖面伪造 token。没有可靠 token 字段，就不会写成“已采集成功”。

第五，桌面 Pulse 只是伴侣。真正的复盘仍然在浏览器 Review 和 Trust 页面里完成。

## 9\. 后续是否继续做

v6 之后，我不打算继续无限追竞品功能。

后续只维护几类事情：

- 上游日志格式变化
- 官方价格变化
- 真实 bug
- 隐私和安全问题
- release / npm / 桌面打包问题

明确不做：云同步、账号体系、多用户、leaderboard、大型 TUI、伪造 collector、文本长度估算 token。

因为再往后加功能，收益已经不如把当前闭环打磨稳定。

## 10\. 排错命令速查

完整下载和启动命令见第 3 节。下面是几个排错或进阶命令。

如果你只想确认它能不能看到你的本机日志，可以先运行：

```
$pkg = 'token-studio' + '@' + '6.0.8'
npx -y $pkg --dry-run-only --no-open
```

如果你已经有本地 SQLite，只想打开看板，不想重新扫描日志：

```
$pkg = 'token-studio' + '@' + '6.0.8'
npx -y $pkg --no-collect
```

如果你要看桌面端实时伴侣，当前推荐先从本地源码或 GitHub Release asset 体验；npm 主入口仍是 Web/CLI：

```bash
git clone https://github.com/RyanCoreAI/token-studio-roi.git
cd token-studio-roi
npm install
npm run desktop
```

项目地址：

如果你想验证它是否真的能采到你本机的数据，最直接的方式还是在本机运行真实模式，而不是看 demo。