---
title: "CC Switch"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
related:
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[DeepSeek]]"
sources:
  - "[[sources/CC Switch 接入国内模型]]"
updated: 2026-06-21
---

# CC Switch

免费开源的跨平台桌面工具，用一个可视化界面统一管理 Claude Code、Codex、Gemini CLI、OpenCode 等多个 AI 编程工具的配置。

- 开源地址：https://github.com/farion1231/cc-switch
- 官网：https://ccswitch.io/
- 内置 50+ 供应商预设（DeepSeek、Qwen、Kimi、智谱 GLM、MiniMax 等）

## 核心能力

### 可视化配置管理
不用手动编辑 JSON/TOML/`.env` 文件，点几下就能一键切换模型。支持从系统托盘快速切换。

### 本地路由（协议转换）
针对 Codex 等使用 Responses API 的工具，CC Switch 在本地启动轻量代理服务做协议转换：
- Codex 发出 Responses API 请求 → CC Switch 转为 Chat Completions API → 发给国内模型
- 整个过程对 Codex 透明

### 安装方式
- **Mac**：`brew install --cask cc-switch`
- **Windows**：下载 `.msi` 安装包
- **Linux**：`.deb` / `.rpm` / `.AppImage`

## 使用场景

1. **Claude Code 接 DeepSeek**：选择预设 → 填 API Key → 启用（无需路由，协议兼容）
2. **Codex 接 DeepSeek**：选择预设 → 填 API Key → 开启本地路由 → 启用（需要协议转换）
3. **其他工具**：类似操作，支持 Gemini CLI、OpenCode 等

## 关联连接
- [[Claude Code]]
- [[Codex]]
- [[DeepSeek]]
- [[智谱 GLM]]
- [[Benchmark vs 任务交付]]
- [[Context Engineering]]
- [[Loop Engineering]]
- [[Vibe Coding]]
- [[Horizon]]
- [[Token Studio ROI]]
