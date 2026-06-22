# 知识库索引

> 内容导向的目录。每个页面一条记录，包含链接和一行摘要。按类别组织。每次 ingest 后更新。

## 总览

- [[wiki/overview|知识库总览]] — AI 编程工具与方法论的全局视图，综合所有来源的演进理解

## 源文件摘要

- [[wiki/sources/Loop Engineering 循环工程|Loop Engineering 循环工程]] — 从 Prompt Engineering 到 Loop Engineering 的 AI 编程范式演进，含 Claude Code/Codex/Cursor 三工具实战
- [[wiki/sources/CC Switch 接入国内模型|CC Switch 接入国内模型]] — 使用 CC Switch 将 Claude Code 和 Codex 切换到 DeepSeek 等国内大模型
- [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]] — Karpathy 提出的 LLM 驱动知识库构建模式，本知识库的理论基础

## 实体

### 工具
- [[wiki/entities/Claude Code|Claude Code]] — Anthropic 推出的终端 AI 编程工具，支持 /goal 和 /loop 命令
- [[wiki/entities/Codex|Codex]] — OpenAI 推出的 AI 编程工具，含 CLI 和桌面 APP 两种形态
- [[wiki/entities/CC Switch|CC Switch]] — 免费开源跨平台工具，统一管理多个 AI 编程工具的模型配置
- [[wiki/entities/Cursor|Cursor]] — AI 编程 IDE，目前无原生 Loop 命令但可通过提示词实现
- [[wiki/entities/Obsidian|Obsidian]] — 本地 Markdown 知识管理工具，LLM Wiki 的浏览器/IDE

### 人物
- [[wiki/entities/程序员鱼皮|程序员鱼皮]] — AI 编程领域博主，多篇教程作者
- [[wiki/entities/Boris Cherny|Boris Cherny]] — Claude Code 之父
- [[wiki/entities/Peter Steinberger|Peter Steinberger]] — OpenClaw 之父
- [[wiki/entities/Andrej Karpathy|Andrej Karpathy]] — LLM Wiki 方法论提出者，Tesla 前 AI 总监、OpenAI 创始成员
- [[wiki/entities/Vannevar Bush|Vannevar Bush]] — Memex 构想提出者（1945），LLM Wiki 的精神前身

### 公司/组织
- [[wiki/entities/Anthropic|Anthropic]] — Claude 和 Claude Code 的开发商
- [[wiki/entities/OpenAI|OpenAI]] — Codex 和 GPT 系列的开发商
- [[wiki/entities/DeepSeek|DeepSeek]] — 国内大模型提供商，支持 Anthropic 兼容协议

## 概念

- [[wiki/concepts/Loop Engineering|Loop Engineering（循环工程）]] — 2026 年中新兴的 AI 编程范式，核心是自动循环 + 反馈闭环
- [[wiki/concepts/Prompt Engineering|Prompt Engineering（提示词工程）]] — 2022-2024 主流范式，关注如何通过对话让 AI 理解需求
- [[wiki/concepts/Context Engineering|Context Engineering（上下文工程）]] — 2025 范式，关注在对的时候把对的信息喂给 AI
- [[wiki/concepts/Harness Engineering|Harness Engineering（驾驭工程）]] — 2026 年初范式，给 AI 搭建靠谱的工作环境（工具+测试+约束）
- [[wiki/concepts/Overbaking|Overbaking（过度烘焙）]] — Loop 运行过久导致 AI 开始乱加功能、乱删测试的现象
- [[wiki/concepts/WorkTree|WorkTree（工作隔离）]] — 多个 Agent 并行工作时使用独立工作目录避免代码冲突
- [[wiki/concepts/MCP|MCP（Model Context Protocol）]] — 模型上下文协议，让 AI 连接外部工具和数据源
- [[wiki/concepts/LLM Wiki 模式|LLM Wiki 模式]] — Karpathy 提出的增量构建+持久化维护的知识库模式（本知识库的元方法论）
- [[wiki/concepts/Memex|Memex]] — Vannevar Bush 1945 年构想的个人知识存储设备，LLM Wiki 精神前身
- [[wiki/concepts/知识复利|知识复利]] — wiki 随每次摄入和查询而增值的核心机制

## 对比

- [[wiki/comparisons/Claude Code vs Codex vs Cursor|Claude Code vs Codex vs Cursor]] — 三大 AI 编程工具的 Loop 能力对比
- [[wiki/comparisons/AI 编程四范式演进|AI 编程四范式演进]] — Prompt → Context → Harness → Loop 的层层递进关系

---

*索引更新时间：2026-06-22*
