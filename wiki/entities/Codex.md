---
title: "Codex"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - codex
related:
  - "[[Claude Code]]"
  - "[[Cursor]]"
  - "[[Loop Engineering]]"
  - "[[CC Switch]]"
  - "[[OpenAI]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
  - "[[sources/CC Switch 接入国内模型]]"
updated: 2026-06-21
---

# Codex

OpenAI 推出的 AI 编程工具，近期热度堪称炸裂。有两种形态：终端 CLI 和桌面 APP。

## 核心特性

### Loop 相关能力
- **`/目标`**：在对话框设定持续运行的目标，AI 持续工作直到达成
- **Automations（自动化面板）**：配置定时执行的自动化任务，如定时总结代码变更、搜集热点资讯

### 模型切换
- 接到国内模型（DeepSeek 等）的关键在于 **协议转换**
- Codex 使用 OpenAI 的 **Responses API**，而国内模型走 **Chat Completions API**
- CC Switch 的「本地路由」功能在本地起轻量代理做协议转换
- 请求流：`Codex → CC Switch → DeepSeek → CC Switch → Codex`
- CLI 和桌面 APP 共用 `~/.codex` 配置，切换一次即可

### 其他
- 内置 WorkTree 支持，可自动创建和管理工作树

## 安装

```bash
npm install -g @openai/codex
```
终端输入 `codex` 进入对话。桌面 APP 需另行下载。

## 与同类工具对比

详见 [[comparisons/Claude Code vs Codex vs Cursor|Claude Code vs Codex vs Cursor]]
