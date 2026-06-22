---
title: "Cursor"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - cursor
related:
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Loop Engineering]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# Cursor

AI 编程 IDE，目前尚无原生的 `/goal` 或 `/loop` 命令。但可以通过在提示词中设计循环机制来实现 Loop Engineering 的思想。

## Loop 实现方式

在提示词中设计自主开发循环的核心要素：

1. **状态追踪**：项目根目录维护 `PROGRESS.md`，记录阶段、进度、问题
2. **开发-验证闭环**：每完成一个模块立即编译验证，有报错就修复
3. **端到端验证**：全部完成后以用户视角做完整测试
4. **防死循环**：同一问题修复超 5 次仍未解决则跳过

这恰好对应 Loop 三要素：目标+停止条件、反馈闭环、状态记忆。

## 与同类工具对比

详见 [[comparisons/Claude Code vs Codex vs Cursor|Claude Code vs Codex vs Cursor]]
