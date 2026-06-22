---
title: "OpenAI"
type: entity
category: company
tags:
  - entity
  - company
  - codex
related:
  - "[[Codex]]"
  - "[[Peter Steinberger]]"
sources:
  - "[[sources/CC Switch 接入国内模型]]"
updated: 2026-06-21
---

# OpenAI

Codex 和 GPT 系列的开发商。其关联工程师 Peter Steinberger 是 Loop Engineering 概念的重要倡导者。

## 相关产品

- **[[Codex]]**：AI 编程工具，含 CLI 和桌面 APP
- **GPT 系列**：大语言模型

## API 协议

OpenAI 使用 **Responses API**（Codex 使用的协议）和 **Chat Completions API**（传统对话协议）。国内模型（DeepSeek 等）通常只支持 Chat Completions API，因此 Codex 接入国内模型需要协议转换（CC Switch 的本地路由功能）。
