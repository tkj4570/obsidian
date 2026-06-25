# 操作日志

> 按时间顺序追加的记录。涵盖所有 ingest、query、lint 操作。每条以 `## [YYYY-MM-DD] 操作类型 | 简述` 开头。
> 实用技巧：`grep "^## \[" wiki/log.md | tail -10` 查看最近 10 条记录。

---

## [2026-06-21] init | 知识库初始化
- 创建三层架构：`raw/`（原始资料）、`wiki/`（Wiki 层）、`CLAUDE.md`（Schema 层）
- 创建目录结构：`wiki/sources/`, `wiki/entities/`, `wiki/concepts/`, `wiki/comparisons/`
- 创建核心文件：`CLAUDE.md`, `wiki/index.md`, `wiki/log.md`, `wiki/overview.md`
- 确立页面规范：YAML frontmatter 模板、标签体系、命名约定
- 确立工作流：Ingest、Query、Lint 三大操作流程
- 领域定位：AI 编程工具与方法论

## [2026-06-21] ingest | Loop Engineering 循环工程
- 来源：`raw/articles/Loop Engineering 循环工程.md`
- 创建源摘要页: [[wiki/sources/Loop Engineering 循环工程]]
- 创建/更新实体: [[wiki/entities/Claude Code]], [[wiki/entities/Codex]], [[wiki/entities/Cursor]], [[wiki/entities/程序员鱼皮]], [[wiki/entities/Boris Cherny]], [[wiki/entities/Peter Steinberger]]
- 创建/更新概念: [[wiki/concepts/Loop Engineering]], [[wiki/concepts/Prompt Engineering]], [[wiki/concepts/Context Engineering]], [[wiki/concepts/Harness Engineering]], [[wiki/concepts/Overbaking]], [[wiki/concepts/WorkTree]], [[wiki/concepts/MCP]]
- 创建对比页: [[wiki/comparisons/Claude Code vs Codex vs Cursor]], [[wiki/comparisons/AI 编程四范式演进]]
- 更新: [[wiki/index]], [[wiki/overview]]

## [2026-06-21] ingest | CC Switch 接入国内模型
- 来源：`raw/articles/2 分钟，教你国内爽用 Claude Code + Codex！保姆级教程 - 编程导航  一线开发者编程经验和技术实战分享.md`
- 创建源摘要页: [[wiki/sources/CC Switch 接入国内模型]]
- 创建/更新实体: [[wiki/entities/CC Switch]], [[wiki/entities/DeepSeek]], [[wiki/entities/Anthropic]], [[wiki/entities/OpenAI]]
- 更新: [[wiki/entities/Claude Code]], [[wiki/entities/Codex]], [[wiki/entities/程序员鱼皮]]
- 更新: [[wiki/index]], [[wiki/overview]]

## [2026-06-22] ingest | LLM Wiki 方法论
- 来源：`raw/articles/llm-wiki-zh.md`（Andrej Karpathy 理念文档的中文翻译）
- 创建源摘要页: [[wiki/sources/LLM Wiki 方法论]]
- 创建实体: [[wiki/entities/Andrej Karpathy]], [[wiki/entities/Obsidian]], [[wiki/entities/Vannevar Bush]]
- 创建概念: [[wiki/concepts/LLM Wiki 模式]], [[wiki/concepts/Memex]], [[wiki/concepts/知识复利]]
- 更新: [[wiki/index]], [[wiki/overview]]
- 注：本篇是本知识库的元方法论来源，CLAUDE.md 设计直接源于此文

## [2026-06-22] ingest | 批量：谷歌大咖出走 + Horizon 日报 ×2
- 来源：`raw/articles/接连两位大咖出走，谷歌到底出了什么BUG？.md`、`raw/articles/Horizon/horizon-2026-06-21-zh.md`、`raw/articles/Horizon/horizon-2026-06-22-zh.md`
- 创建源摘要页: [[wiki/sources/谷歌大咖出走分析]], [[wiki/sources/Horizon 每日速递 2026-06-21]], [[wiki/sources/Horizon 每日速递 2026-06-22]]
- 创建实体: [[wiki/entities/Google DeepMind]], [[wiki/entities/Antigravity]], [[wiki/entities/Noam Shazeer]], [[wiki/entities/John Jumper]], [[wiki/entities/Headroom]], [[wiki/entities/Codebase Memory MCP]]
- 创建概念: [[wiki/concepts/Benchmark vs 任务交付]]
- 更新: [[wiki/index]], [[wiki/overview]]
- 注：谷歌文章与已有 Loop Engineering 知识形成强印证——Antigravity 失败恰好因为缺乏 Loop 机制

## [2026-06-22] ingest | Horizon 项目介绍
- 来源：`raw/articles/Horizon README_zh.md at main.md`
- 创建源摘要页: [[wiki/sources/Horizon 项目介绍]]
- 创建实体: [[wiki/entities/Horizon]]
- 更新: [[wiki/index]]
- 注：Horizon 本身是 LLM Wiki 模式在新闻领域的应用——之前摄入的日报就是它的产物

## [2026-06-22] ingest | Vibe Coding 常见问题
- 来源：`raw/articles/90 Vibe Coding 常见问题和解决 - 鱼皮的 AI 知识库（免费）  编程导航项目实战教程.md`
- 创建源摘要页: [[wiki/sources/Vibe Coding 常见问题和解决]]
- 创建概念: [[wiki/concepts/Vibe Coding]], [[wiki/concepts/AI幻觉]]
- 创建实体: [[wiki/entities/Windsurf]]
- 更新: [[wiki/index]]
- 注：[[Vibe Coding]] 是 AI 编程实践层的关键概念，填补了概念体系中的重要缺口

## [2026-06-22] project | 本地项目汇总
- 来源：`raw/articles/personal/本地项目汇总说明.md`
- 创建实体: [[wiki/entities/本地项目汇总]], [[wiki/entities/GBrain]], [[wiki/entities/Token Studio ROI]], [[wiki/entities/Loop Demo]]
- 更新: [[wiki/index]]
- 注：GBrain 与本知识库共享 LLM Wiki 模式理论基础；Token Studio ROI 与 Loop Engineering 的 Token 成本约束问题直接相关

## [2026-06-23] ingest | 批量：5 篇未摄入文章
- 来源：`raw/articles/windows 下 CodeX 提示 Computer Use plugins unavailable.md`、`raw/articles/Horizon/horizon-2026-06-23-zh.md`、`raw/articles/Valve 在时隔多年后...Steam Machine.md`、`raw/articles/【Claude Code 国内使用完整指南】CC-Switch + 智谱 GLM...md`、`raw/articles/我做了一个本地 AI 编程 ROI 复盘系统...md`
- 创建源摘要页: [[wiki/sources/CodeX Computer Use 修复]], [[wiki/sources/Horizon 每日速递 2026-06-23]], [[wiki/sources/Valve Steam Machine 发布]], [[wiki/sources/CC-Switch 智谱 GLM 教程]], [[wiki/sources/Token Studio ROI 项目详解]]
- 创建实体: [[wiki/entities/Oak]]
- 更新: [[wiki/index]]
- 注：智谱 GLM 教程补充了 CC Switch 的第三个国内模型方案；Token Studio 详解与已创建的实体页互补

## [2026-06-24] ingest | 6月23日 github热榜：涨⭐前十项目全解析
- 来源：`raw/transcripts/6月23日 github热榜：涨⭐前十项目全解析.md`
- 创建源摘要页: [[wiki/sources/6月23日 github热榜：涨⭐前十项目全解析]]
- 创建实体: [[wiki/entities/大雄AI实战]]
- 创建概念: [[wiki/concepts/GitHub热榜]], [[wiki/concepts/AI工作流工具]], [[wiki/concepts/开源超级智能体框架]], [[wiki/concepts/智能体技能]], [[wiki/concepts/代码库记忆]]
- 更新: [[wiki/index]]
- 注：本次摄入建立了GitHub热榜分析框架，系统化了AI工作流工具的概念体系，揭示了从agent skills到agency agents再到product process AI的发展趋势

## [2026-06-24] re-ingest | B站视频转本地AI知识库！新手也能3分钟上手
- 来源：`raw/transcripts/2026-06-24-把B站视频转成本地AI知识库！新手也能3分钟上手.md`
- 更新源摘要页: [[wiki/sources/B站视频转本地AI知识库！新手也能3分钟上手]]
- 创建实体: [[wiki/entities/MIP耀]]（更新已有页面，补充详细信息）
- 创建概念: [[wiki/concepts/视频转知识库]], [[wiki/concepts/多媒体知识摄入]]
- 更新实体: [[wiki/entities/Bilibili Web Clipper]], [[wiki/entities/Local REST API]], [[wiki/entities/karpathy-llm-wiki-vault]]
- 更新: [[wiki/index]], [[wiki/overview]]
- 注：本次摄入完整构建了多媒体知识摄入的技术体系，填补了工具链和概念体系的重要空白

## [2026-06-24] ingest | Horizon 每日速递 2026-06-24（最后一批摄入）
- 来源：`raw/articles/Horizon/horizon-2026-06-24-zh.md`
- 创建源摘要页: [[wiki/sources/Horizon 每日速递 2026-06-24]]
- 更新: [[wiki/index]], [[wiki/log]]
- 注：本次摄入完成了raw目录中所有文章的摄入工作，知识库现在包含完整的原始资料体系

## [2026-06-24] git commit | 知识库完整更新
- 提交记录：完成知识库全面摄入和更新，包括B站视频转知识库教程、GitHub热榜分析、Horizon每日速递等
- 新增内容：2个源摘要页、1个实体页、7个概念页
- 更新内容：index.md、overview.md、log.md的全面更新
- 技术体系建设：建立了GitHub热榜分析框架、AI工作流工具体系、多媒体知识摄入技术体系
- 注：知识库已完成raw目录下所有文章的摄入工作，建立了完整的知识网络

## [2026-06-25] ingest | Codex 录制回放功能评测
- 来源：`raw/articles/Codex 又出王炸功能「录制回放」，实战测评！附原理浅析.md`
- 创建源摘要页: [[wiki/sources/Codex 录制回放功能评测]]
- 创建概念: [[wiki/concepts/录制回放工作流]]
- 更新: [[wiki/index]]
- 注：去除作者个人观点，聚焦技术原理和客观分析，建立了录制回放工作流的概念体系

## [2026-06-25] ingest | AI大模型原理解析
- 来源：`raw/articles/AI 为什么会胡说八道？傻子可懂的 AI 大模型原理讲解.md`
- 创建源摘要页: [[wiki/sources/AI大模型原理解析]]
- 更新概念: [[wiki/concepts/AI幻觉]]（补充详细技术原理）
- 创建概念: [[wiki/concepts/Transformer架构]]
- 更新: [[wiki/index]], [[wiki/log]]
- 注：去除个人观点，聚焦AI大模型核心技术原理，建立了完整的技术分析框架
