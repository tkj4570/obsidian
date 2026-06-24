---
title: "Claude Code"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - claude-code
related:
  - "[[Codex]]"
  - "[[Cursor]]"
  - "[[Loop Engineering]]"
  - "[[CC Switch]]"
  - "[[Anthropic]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
  - "[[sources/CC Switch 接入国内模型]]"
updated: 2026-06-21
---

# Claude Code

Anthropic 推出的 AI 编程工具，直接在终端中运行。通过对话描述需求，AI 能自主分析项目、写代码、跑命令、修 Bug，全程自主执行。

## 核心特性

### Loop 相关命令
- **`/goal`**：让 AI 持续工作直到设定目标达成。每轮结束由独立小模型判断目标是否达成。适合有明确终点的一次性任务（模块迁移、批量重构等）。
- **`/loop`**：按固定时间间隔定时循环执行操作。适合持续监控场景（检查部署状态、扫描安全漏洞等）。

### 其他特性
- `--worktree` 参数支持独立工作树，用于多 Agent 并行工作隔离
- 支持通过 CC Switch 切换模型供应商（包括 DeepSeek 等国内模型）
- DeepSeek 提供了兼容 Anthropic 协议的 Messages API，Claude Code 接入特别简单

## 安装

```bash
npm install -g @anthropic-ai/claude-code
```
前提：Node.js 环境。终端输入 `claude` 进入对话界面。

## 与同类工具对比

| 特性 | Claude Code | Codex | Cursor |
|------|-------------|-------|--------|
| Loop 支持 | `/goal` + `/loop`（原生） | `/目标` + Automations | 无原生，靠提示词 |
| 界面 | 终端 CLI | CLI + 桌面 APP | IDE |
| 模型切换 | CC Switch 直接配置 | CC Switch + 本地路由 | 内置 |

详见 [[comparisons/Claude Code vs Codex vs Cursor|Claude Code vs Codex vs Cursor]]

## 关联连接
- [[Codex]]
- [[Cursor]]
- [[Loop Engineering]]
- [[CC Switch]]
- [[Anthropic]]
- [[Harness Engineering]]
- [[WorkTree]]
- [[MCP]]
- [[Context Engineering]]
- [[Vibe Coding]]
- [[Benchmark vs 任务交付]]
- [[知识复利]]
- [[Overbaking]]
