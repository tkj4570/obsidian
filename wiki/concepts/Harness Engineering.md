---
title: "Harness Engineering（驾驭工程）"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Context Engineering]]"
  - "[[Loop Engineering]]"
  - "[[WorkTree]]"
  - "[[MCP]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# Harness Engineering（驾驭工程）

2026 年初兴起的 AI 编程范式。关注的是**给 AI 搭建一整套靠谱的工作环境**。

## 核心组成

- **工具配备**：给 AI 配备执行任务所需的工具（运行命令、访问文件、调用 API 等）
- **任务拆解**：把大任务拆成可验证的小步骤
- **测试搭建**：有自动测试来验证 AI 产出的代码是否正确
- **架构约束**：防止代码腐烂，保持代码质量

## 类比

如果把 AI 比作一匹马，Harness 就是你给马装上的缰绳、马鞍和围栏。把 Harness 搭好之后，AI 才能在一个有工具、有测试、有约束的环境里稳定可靠地产出。

## 与 Loop 的关系

- Harness 是 Loop 的基础——Loop 里的反馈闭环依赖 Harness 搭建的测试和工具
- Loop 在 Harness 之上加了一层"自动循环"机制
- 很多人容易把两者搞混：Harness 是骑马时你手动驾驭缰绳；Loop 是设定巡逻路线后让马自己跑

## 在演进中的位置

位于 Context Engineering 之上，Loop Engineering 之下。详见 [[comparisons/AI 编程四范式演进|AI 编程四范式演进]]。

## 关联连接
- [[Context Engineering]]
- [[Loop Engineering]]
- [[WorkTree]]
- [[MCP]]
- [[Claude Code]]
- [[Codex]]
- [[Benchmark vs 任务交付]]
- [[Vibe Coding]]
