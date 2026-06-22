---
title: "Claude Code vs Codex vs Cursor"
type: comparison
tags:
  - comparison
  - ai-programming
  - tool
related:
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Cursor]]"
  - "[[Loop Engineering]]"
updated: 2026-06-21
---

# Claude Code vs Codex vs Cursor

三大主流 AI 编程工具的全方位对比（以 Loop Engineering 能力为核心视角）。

## 概览对比

| 维度 | Claude Code | Codex | Cursor |
|------|-------------|-------|--------|
| **开发商** | [[Anthropic]] | [[OpenAI]] | Cursor Inc. |
| **形态** | 终端 CLI | CLI + 桌面 APP | IDE |
| **原生 Loop** | ✅ `/goal` + `/loop` | ✅ `/目标` + Automations | ❌ 无原生 |
| **调度方式** | 目标驱动 / 定时循环 | 目标驱动 / 定时自动化 | 提示词驱动 |
| **模型切换** | 简单（兼容协议） | 需路由（协议不同） | 内置 |
| **WorkTree** | ✅ `--worktree` | ✅ 内置 | ✅ 内置 |
| **安装方式** | `npm install -g @anthropic-ai/claude-code` | `npm install -g @openai/codex` | IDE 下载 |

## Loop 能力详解

### Claude Code
- **`/goal`**：持续工作直到目标达成。独立小模型判断完成状态。适合有明确终点的一次性任务。
- **`/loop`**：定时循环。适合持续监控（部署状态、安全漏洞）。
- 可加熔断限制（如"20 轮还没搞定就停"）。
- **最成熟的 Loop 实现**。

### Codex
- **`/目标`**：与 Claude Code 的 `/goal` 类似，设定目标后 AI 持续推进。
- **Automations**：定时自动化面板，支持自定义和执行内置模板。
- 接入国内模型需开启 CC Switch 本地路由（协议转换）。

### Cursor
- **无原生 Loop 命令**。
- 可通过提示词设计实现：在提示词中写明状态追踪、开发-验证闭环、防死循环规则。
- 需要更多手动设计和调试。

## 接入国内模型对比

| 工具 | 接入方式 | 难度 | 原理 |
|------|---------|------|------|
| Claude Code | CC Switch 直接配置 | ⭐ | Messages API 兼容 |
| Codex | CC Switch + 本地路由 | ⭐⭐⭐ | 需 Responses API 转换 |
| Cursor | 内置模型设置 | ⭐ | IDE 内置支持 |

## 选型建议

- **体验最新 Loop 范式**：Claude Code（`/goal` 最成熟）
- **图形界面 + Loop**：Codex 桌面 APP（Automations 面板直观）
- **传统 IDE 工作流 + 灵活提示词**：Cursor
- **预算有限 / 用国内模型**：Claude Code 接入最简单
