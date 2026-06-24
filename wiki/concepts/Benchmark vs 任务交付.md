---
title: "Benchmark vs 任务交付"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
  - ai-agent
related:
  - "[[Loop Engineering]]"
  - "[[Harness Engineering]]"
  - "[[Antigravity]]"
  - "[[Overbaking]]"
sources:
  - "[[sources/谷歌大咖出走分析]]"
updated: 2026-06-22
---

# Benchmark vs 任务交付

AI Agent 产品评价范式之争。核心论点：**benchmark 分数高 ≠ 能交付任务**。

## 数学本质

单步正确率 95% 的模型，连续 20 步不出错的概率仅 **0.95^20 ≈ 36%**。即使提升到 98%，20 步全部顺利的概率也只有 **67%**。

Agent 任务不是单轮问答，而是几十步的连续操作——每一步都可能失败。

## 真正的护城河

不是把 benchmark 再刷高两分，而是给以下能力做出可靠机制：

- **错误恢复**：失败了能自动重试/回退
- **状态保存**：中间状态持久化，断点可恢复
- **权限确认**：危险操作需要确认
- **人工接管**：关键节点允许人类介入
- **回滚**：出了问题能回到上一个已知状态
- **结果验证**：不是"模型说它做完了"而是"可验证地做完了"

这正是 [[Loop Engineering]] 三要素中的**反馈闭环**和**状态记忆**。

## 案例：Antigravity

谷歌的 [[Antigravity]] 2.0 就是反面教材——benchmark 叙事完美，但缺乏上述机制，实际交付能力差。而 [[Claude Code]] 的 `/goal` 命令恰好内置了这些机制（独立判断模型验证完成状态、熔断限制、循环状态追踪）。

## 与已有概念的关联

- [[Loop Engineering]]：反馈闭环正是解决"多步累积错误"的核心
- [[Overbaking]]：如果只有"跑到通过"而没有合理约束，就是 Overbaking
- [[Harness Engineering]]：给 AI 搭靠谱环境，本质上就是建立这些交付保障机制

## 关联连接
- [[Loop Engineering]]
- [[Harness Engineering]]
- [[Antigravity]]
- [[Overbaking]]
- [[Claude Code]]
- [[Codex]]
- [[Context Engineering]]
- [[知识复利]]
