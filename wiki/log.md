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
