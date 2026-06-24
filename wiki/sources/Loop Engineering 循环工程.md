---
title: "Loop Engineering 循环工程"
type: source
source_url: "https://ai.codefather.cn/post/2066793761979092994"
author: "[[程序员鱼皮]]"
published: 2026-06-21
ingested: 2026-06-21
tags:
  - source
  - ai-programming
  - methodology
related:
  - "[[Loop Engineering]]"
  - "[[Prompt Engineering]]"
  - "[[Context Engineering]]"
  - "[[Harness Engineering]]"
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Cursor]]"
---

# Loop Engineering 循环工程

> 来源：程序员鱼皮，2026.06 | [原文链接](https://ai.codefather.cn/post/2066793761979092994)

## 核心观点

1. **AI 编程范式正在升级**：从手动写提示词（Prompt Engineering）向设计循环系统（Loop Engineering）转变。Claude Code 之父 Boris Cherny 和 OpenClaw 之父 Peter Steinberger 同时倡导这一方向。

2. **Loop Engineering 的定义**：设计一套自动运转的系统，让它代替你去给 AI 下达指令、检查 AI 输出、记录进度、决定下一步，不断循环直到达成预设目标。类比：从"开手动挡车"到"自动驾驶"。

3. **Loop 三要素**：
   - **明确的目标和停止条件**（可验证的，如"所有测试通过"）
   - **反馈闭环**（每轮检查结果，决定继续还是停止）
   - **状态记忆**（外部文件记录进度，断点可恢复）

4. **AI 编程四范式层层包含**：Prompt Engineering → Context Engineering → Harness Engineering → Loop Engineering。后者不是取代前者，而是建立在前者基础上。

5. **三大工具对比**：Claude Code 内置 `/goal` 和 `/loop`（最成熟）；Codex 有 `/目标` 和 Automations；Cursor 无原生支持但可通过提示词实现。

## 关键引用

> "我不再提示 Claude 了，我有一堆循环在运行，它们才是在提示 Claude 并判断接下来该做什么。我的工作变成了写循环。" — Boris Cherny

> "你不该再给编程 Agent 写提示词了。你应该设计一套循环机制，让这些循环去提示你的 Agent。" — Peter Steinberger

## 涉及的新概念

- [[Loop Engineering|Loop Engineering（循环工程）]]
- [[Overbaking|Overbaking（过度烘焙）]]
- [[WorkTree|WorkTree（工作隔离）]]
- [[MCP|MCP（Model Context Protocol）]]

## 涉及的工具/实体

- [[Claude Code]] — `/goal` 和 `/loop` 命令
- [[Codex]] — `/目标` 和 Automations
- [[Cursor]] — 无原生 Loop，通过提示词设计实现
- [[程序员鱼皮]] — 作者
- [[Boris Cherny]] — Claude Code 之父
- [[Peter Steinberger]] — OpenClaw 之父

## 实用要点

- Token 成本是真实约束：高频循环消耗大，需权衡价值
- 调试比提示词难 10 倍：从简单的 Loop 做起，设小目标
- Overbaking 风险：设循环上限，写清楚做/不做什么
- 学习路径：先打好 Prompt/Context/Harness 基础，再上 Loop

## 关联连接
- [[Loop Engineering]]
- [[Prompt Engineering]]
- [[Context Engineering]]
- [[Harness Engineering]]
- [[Claude Code]]
- [[Codex]]
- [[Cursor]]
- [[程序员鱼皮]]
- [[Boris Cherny]]
- [[Peter Steinberger]]
- [[Overbaking]]
- [[WorkTree]]
- [[MCP]]
- [[Benchmark vs 任务交付]]
- [[Vibe Coding]]
- [[AI幻觉]]
- [[知识复利]]
