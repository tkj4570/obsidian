---
title: "CC-Switch + 智谱 GLM Coding Plan 全流程教程"
type: source
source_url: "https://blog.csdn.net/weixin_44262492/article/details/160348230"
author: "weixin_44262492"
published: 2026-04-20
ingested: 2026-06-23
tags:
  - source
  - ai-programming
  - tool
  - claude-code
related:
  - "[[CC Switch]]"
  - "[[Claude Code]]"
  - "[[DeepSeek]]"
---

# CC-Switch + 智谱 GLM Coding Plan 教程

> 国内使用 Claude Code 的完整方案。费用约为官方 1/7，额度 3 倍，无需代理。

## 核心方案

- **CC-Switch** 可视化配置 → **智谱 GLM Coding Plan** API → Claude Code 终端使用
- Coding 专用端点：`https://open.bigmodel.cn/api/anthropic`
- 模型：GLM-5.1（Opus级）、GLM-5-Turbo（Sonnet级）、GLM-4.7（Haiku级）
- 套餐：¥20/月起（Lite），高峰期 GLM-5.1 消耗 3×

## 与已有知识的关联

- 这是 [[CC Switch]] 接入国内模型的第三个方案（继 DeepSeek 后），补充了智谱 GLM 这一选项
- 与 [[sources/CC Switch 接入国内模型|CC Switch 接入 DeepSeek]] 形成对照：DeepSeek 兼容协议不需路由，智谱同样通过 Anthropic 兼容端点直连
