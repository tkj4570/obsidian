---
title: "AI 编程四范式演进"
type: comparison
tags:
  - comparison
  - ai-programming
  - methodology
related:
  - "[[Prompt Engineering]]"
  - "[[Context Engineering]]"
  - "[[Harness Engineering]]"
  - "[[Loop Engineering]]"
updated: 2026-06-21
---

# AI 编程四范式演进

从 2022 年到 2026 年，AI 编程领域经历了四个层层递进的范式。理解这个演进历程是理解当前 AI 编程工具设计思想的关键。

## 演进概览

```
Prompt Engineering (2022-2024)
    ↓ 怎么让 AI 理解你说的话
Context Engineering (2025)
    ↓ 怎么让 AI 了解你的项目背景
Harness Engineering (2026初)
    ↓ 怎么给 AI 搭建靠谱的工作环境
Loop Engineering (2026中)
    ↓ 怎么让 AI 自己跑起来
```

## 四个范式对比

| 维度 | Prompt Eng. | Context Eng. | Harness Eng. | Loop Eng. |
|------|-------------|--------------|--------------|-----------|
| **时间** | 2022-2024 | 2025 | 2026 初 | 2026 中 |
| **核心问题** | AI 答非所问 | AI 脱离实际 | AI 产出不可靠 | 需要手动推着走 |
| **关键方法** | 角色设定、思维链 | AGENTS.md、RAG、记忆 | 工具配备、测试、约束 | 自动循环+反馈闭环 |
| **类比** | 学会跟马说话 | 让马了解路线 | 给马装缰绳马鞍 | 让马自己巡逻 |
| **人的角色** | 提示词写手 | 上下文管理者 | 环境搭建者 | 规则设计师 |

## 层层包含关系

这四个范式不是取代关系，而是**层层包含**：

- Loop Engineering 用到了 Harness Engineering 搭建的测试和工具
- Harness Engineering 需要 Context Engineering 提供的项目上下文
- Context Engineering 建立在 Prompt Engineering 的对话技巧之上

**Loop 不会让提示词"死亡"**——它只是让这些基础能力通过循环机制自动运转起来。

## 当前状态（2026.06）

- Loop Engineering 仍是**早期概念**，业界尚无统一标准和最佳实践
- Anthropic（Claude Code）和 OpenAI（Codex）都在推进这一方向
- 建议学习路径：先打好 Prompt/Context/Harness 基础，再从轻量 `/goal` 开始体验 Loop
