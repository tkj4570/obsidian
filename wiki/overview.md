---
title: "知识库总览"
type: overview
tags:
  - overview
  - ai-programming
updated: 2026-06-22
---

# AI 编程工具与方法论 — 知识库总览

## 本知识库是什么

这是一个关于 **AI 编程工具与方法论** 的个人知识库。它由 LLM 增量构建和维护，基于用户策展的原始资料，持续积累对 AI 编程领域的理解。

**本知识库本身是 LLM Wiki 模式的一个实例**——它的架构、工作流和演进方式直接遵循 [[Andrej Karpathy]] 的 [[LLM Wiki 模式|LLM Wiki 方法论]]。详见 [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]]。

核心关注点：
- **AI 编程工具**：Claude Code、Codex、Cursor 等工具的原理、用法和对比
- **AI 编程范式**：从 Prompt Engineering 到 Loop Engineering 的演进历程
- **知识管理方法**：LLM Wiki 模式、知识复利机制、Schema 共演进
- **实用技巧**：模型切换、配置优化、工作流设计

## 当前知识结构

### AI 编程范式的演进

```
Prompt Engineering (2022-2024)
    ↓ 关注「如何让 AI 理解需求」
Context Engineering (2025)
    ↓ 关注「如何在对的时候给 AI 对的上下文」
Harness Engineering (2026初)
    ↓ 关注「如何给 AI 搭建靠谱工作环境」
Loop Engineering (2026中)
    ↓ 关注「如何让 AI 自己形成工作循环」
```

这是 AI 编程领域最核心的叙事线——从"手动挡"到"自动驾驶"的进化。详见 [[wiki/comparisons/AI 编程四范式演进|AI 编程四范式演进]]。

### 当前局面

截至 2026 年 6 月，Loop Engineering 是一个**早期概念**，业界尚无统一标准。两家头部公司（Anthropic 和 OpenAI）的工程师都在倡导这一方向，但最佳实践仍在探索中。

三大 AI 编程工具的 Loop 支持状态：
- [[wiki/entities/Claude Code|Claude Code]]：内置 `/goal` 和 `/loop`，最成熟
- [[wiki/entities/Codex|Codex]]：内置 `/目标` 和 Automations，需开启本地路由才能接国内模型
- [[wiki/entities/Cursor|Cursor]]：无原生支持，可通过提示词设计实现

### 已确认的关键洞察

1. **Loop 不是取代提示词的**——它是建立在提示词、上下文、Harness 之上的更高层抽象（四者层层包含）

2. **Loop 三要素**：明确目标+停止条件、反馈闭环、状态记忆——这三样缺一不可

3. **Token 成本是真实约束**——高频循环的 token 消耗不可忽视，需要在实际价值和成本间权衡

4. **Overbaking 是真实风险**——Loop 跑太久会开始"加戏"，需要合理的循环次数上限

5. **基础不牢，Loop 只是放大问题**——先打好 Prompt/Context/Harness 的基础再上 Loop

6. **知识复利是实现长期价值的关键**——LLM Wiki 和 Loop Engineering 共享同一底层逻辑：让 LLM 做簿记，让每次交互的产出持久积累而非消失在聊天记录中

### 跨领域连接

- **LLM Wiki ↔ Loop Engineering**：两个看似不相关的概念共享核心思想——LLM 做持续的簿记工作，人类做策展和决策。LLM Wiki 中"好答案归档回 wiki"的 Query 复利，与 Loop Engineering 中"状态记忆让循环不归零"的设计完全同构。详见 [[知识复利]]。

### 待探索的方向

- Loop Engineering 的最佳实践和设计模式
- 多个 Agent 并行协作的 WorkTree 隔离策略（已有概念，缺乏实战）
- MCP 协议在 AI 编程工具连接中的实际应用
- 国内模型（DeepSeek、Qwen 等）在 AI 编程场景中的表现对比
- 不同工具的 Skills/技能沉淀机制对比

### 来源清单

当前知识库基于以下原始资料构建：

1. [[wiki/sources/Loop Engineering 循环工程|Loop Engineering 循环工程]] — 鱼皮，2026.06
2. [[wiki/sources/CC Switch 接入国内模型|CC Switch 接入国内模型]] — 鱼皮，2026.06
3. [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]] — Andrej Karpathy，2026.06（本知识库的元方法论）

---

*本页面是所有 ingest 和 query 的综合产物，随新来源的加入和新问题的探索持续演进。*
