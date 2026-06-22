---
title: "DeepSeek"
type: entity
category: company
tags:
  - entity
  - company
  - llm
related:
  - "[[CC Switch]]"
  - "[[Claude Code]]"
  - "[[Codex]]"
sources:
  - "[[sources/CC Switch 接入国内模型]]"
updated: 2026-06-21
---

# DeepSeek

国内大模型提供商，是 AI 编程工具接入国内模型的首选方案之一。

## 核心优势

- **价格便宜**：API 价格远低于 Anthropic/OpenAI 官方
- **协议兼容**：提供**兼容 Anthropic Messages API** 的接口，Claude Code 可直接接入无需协议转换
- **模型能力**：DeepSeek-V4-Pro（Agent 能力和复杂推理强）、DeepSeek-V4-Flash（轻量快速）
- **超长上下文**：支持 1M tokens 模式

## 接入 AI 编程工具

| 工具 | 接入难度 | 原因 |
|------|---------|------|
| [[Claude Code]] | ⭐ 简单 | Messages API 协议兼容，直接配置 |
| [[Codex]] | ⭐⭐⭐ 需路由 | 需要 CC Switch 本地路由做协议转换 |

## 获取 API Key

1. 注册登录 [DeepSeek 开放平台](https://platform.deepseek.com/)
2. 进入 API keys 页面创建 key
3. ⚠️ Key 只在创建时完整显示一次，务必当场保存
