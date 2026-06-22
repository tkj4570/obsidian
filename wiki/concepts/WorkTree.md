---
title: "WorkTree（工作隔离）"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Loop Engineering]]"
  - "[[Harness Engineering]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# WorkTree（工作隔离）

Loop Engineering 五大模块之一（工作隔离）。当多个 AI Agent 同时在一个项目干活时，使用 Git WorkTree 给每个 Agent 分配独立的工作目录。

## 解决的问题

多个 Agent 并行工作时，可能同时修改同一个文件（如主页），导致代码冲突，乱成一团。

## 实现方式

- 给每个 Agent 分配独立的 Git WorkTree，各自在自己的分支上开发
- 互不干扰，最后再合并回主干
- [[Claude Code]] 通过 `--worktree` 参数启动独立工作树
- [[Codex]] 和 [[Cursor]] 的 Agent 面板也都内置了 WorkTree 支持

## 在 Loop 中的角色

属于进阶优化——基础循环跑起来之后再考虑，不需要一上来就全部配齐。
