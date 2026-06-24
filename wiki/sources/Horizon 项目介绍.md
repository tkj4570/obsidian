---
title: "Horizon 项目介绍"
type: source
source_url: "https://github.com/Thysrael/Horizon"
author: "Thysrael"
published: 2026
ingested: 2026-06-22
tags:
  - source
  - ai-programming
  - tool
  - news
related:
  - "[[Horizon]]"
  - "[[MCP]]"
---

# Horizon 项目介绍

> 来源：Thysrael | [GitHub](https://github.com/Thysrael/Horizon)

## 核心定位

Horizon 是一个**开源的 AI 新闻雷达**——从多个信息源抓取内容，用 AI 打分过滤、去重、补充背景、总结评论，生成中英双语日报。

一句话标语：**"你只需享受新闻，剩下交给 Horizon。"**

## 工作流（Pipeline）

```
多源抓取 → 去重合并 → AI 打分过滤 → 背景补充 → 评论总结 → 多渠道分发
```

- **抓取**：Hacker News、Reddit、Telegram、RSS、Twitter/X、GitHub、OpenBB
- **打分**：支持 Claude、GPT、Gemini、DeepSeek、豆包、MiniMax 等模型评分 0-10
- **分发**：GitHub Pages、邮件、飞书/钉钉/Slack/Discord Webhook、MCP Server

## 与本知识库的关系

我们已摄入的两篇 Horizon 日报（[[sources/Horizon 每日速递 2026-06-21|6-21]] / [[sources/Horizon 每日速递 2026-06-22|6-22]]）正是由这个工具生成的。Horizon 本身是一个 **LLM Wiki 模式在新闻领域的应用**——LLM 每天自动筛选、整理、分发信息，人类只需消费结果。

## 涉及的新实体

- [[Horizon]] — 工具本身

## 关联连接
- [[Horizon]]
- [[MCP]]
- [[LLM Wiki 模式]]
- [[本地项目汇总]]
- [[GBrain]]
- [[Token Studio ROI]]
- [[Claude Code]]
- [[Benchmark vs 任务交付]]
- [[Codebase Memory MCP]]
- [[Headroom]]
