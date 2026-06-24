---
title: CC Switch 接入国内模型
type: source
source_url: https://www.codefather.cn/post/2064234894459990018
author: "[[程序员鱼皮]]"
published: 2026-06-21
ingested: 2026-06-21
tags:
  - source
  - ai-programming
  - tool
related:
  - "[[CC Switch]]"
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Valve 在时隔多年后，正式发布了一款全新的游戏硬件Steam Machine]]"
---

# CC Switch 接入国内模型

> 来源：程序员鱼皮，2026.06 | [原文链接](https://www.codefather.cn/post/2064234894459990018)

## 核心观点

1. **AI 编程工具的门槛正在消失**：通过开源工具 + 国内大模型，几分钟就能把 Claude Code、Codex 跑起来，成本可能只有官方的零头。

2. **CC Switch 解决了多工具模型配置的痛点**：Claude Code、Codex、Gemini CLI、OpenCode 等工具的配置格式各不相同，CC Switch 用一个可视化界面统一管理，内置 50+ 供应商预设。

3. **Claude Code 接 DeepSeek 特别简单**：因为 DeepSeek 提供了兼容 Anthropic 协议的接口（Messages API），CC Switch 直接写配置即可生效，无需协议转换。

4. **Codex 接国内模型需要协议转换**：Codex 用的是 OpenAI 的 Responses API，而 DeepSeek 等国内模型走的是 Chat Completions API。CC Switch 的「本地路由」功能在本地起一个轻量代理做协议转换。

5. **模型与实际回复的关系**：AI 可能嘴上说自己是 GPT-5（因为系统提示词），但实际干活的底层已经换成 DeepSeek 了。需要理解模型身份与实际运行模型的区别。

## 涉及的新实体

- [[CC Switch]] — 开源跨平台模型切换工具
- [[Valve 在时隔多年后，正式发布了一款全新的游戏硬件Steam Machine]] — 国内大模型提供商，支持 Anthropic 兼容协议

## 涉及的工具/实体（更新）

- [[Claude Code]] — 通过 CC Switch 切换模型
- [[Codex]] — 需要开启本地路由才能接国内模型
- [[程序员鱼皮]] — 作者
- [[Anthropic]] — Claude Code 开发商
- [[OpenAI]] — Codex 开发商

## 技术要点

### Claude Code 接入流程
```
安装 Claude Code → CC Switch 选 DeepSeek 预设 → 填入 API Key → 启用
```
原理：DeepSeek 的 Messages API 兼容 Anthropic 协议，直接通信。

### Codex 接入流程
```
安装 Codex → CC Switch 选 DeepSeek 预设 → 填入 API Key → 开启本地路由 → 启用
```
原理：CC Switch 本地代理做 Responses API ↔ Chat Completions API 协议转换。
请求流：`Codex → CC Switch → DeepSeek → CC Switch → Codex`

## 实用要点

- CC Switch 开源地址：https://github.com/farion1231/cc-switch
- Windows 用 `.msi` 安装包，Mac 可用 Homebrew
- API Key 只在创建时完整显示一次，务必当场保存
- 切回官方模型只需反向操作：关路由、启用默认配置
- 其他国内模型（Qwen、Kimi、智谱 GLM）操作几乎一样
