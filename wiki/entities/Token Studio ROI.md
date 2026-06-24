---
title: "Token Studio ROI"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - token-optimization
related:
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Loop Engineering]]"
  - "[[Headroom]]"
sources:
  - "[[wiki/entities/本地项目汇总|本地项目汇总]]"
updated: 2026-06-22
---

# Token Studio ROI

鱼皮开发的本地 AI 编程 ROI 复盘系统。核心问题：**"AI 编程花掉的 Token，到底换来了什么？"**

- 仓库：https://github.com/RyanCoreAI/token-studio-roi
- npm：`token-studio` (v6.0.8)
- 本地：`D:\php_code\ai_project\token-studio-roi-main`

## 核心功能

| 功能 | 说明 |
|------|------|
| 真实本地采集 | 读取 Claude Code/Codex CLI 的结构化 Token 日志 |
| Evidence Flywheel | Token 消耗 → 项目 → 任务 → 产出（PR/commit） |
| ROI Advisor | 本地规则判断：高成本无产出、模型选择不当等 |
| Desktop Pulse | 桌面看板，监控 24h Token 是否失控 |
| Savings Simulator | 模拟模型切换后的节省空间 |

## 隐私保护

- 不保存 prompt、response、对话正文、diff
- 数据全在本地 SQLite，不上传云端
- Web API 默认绑定 127.0.0.1

## 与已有知识的关联

- [[Loop Engineering]] 中提到的 Token 成本约束问题 → Token Studio 就是解决这个的
- [[Headroom]] — 另一个 Token 优化工具（压缩输入），Token Studio 侧重复盘
- [[Claude Code]] / [[Codex]] — 主要数据来源

## 关联连接
- [[Claude Code]]
- [[Codex]]
- [[Loop Engineering]]
- [[Headroom]]
- [[本地项目汇总]]
- [[Benchmark vs 任务交付]]
- [[知识复利]]
- [[Context Engineering]]
- [[Vibe Coding]]
