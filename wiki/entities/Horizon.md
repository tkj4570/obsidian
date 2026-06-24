---
title: "Horizon"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - news
related:
  - "[[MCP]]"
  - "[[LLM Wiki 模式]]"
sources:
  - "[[sources/Horizon 项目介绍]]"
  - "[[sources/Horizon 每日速递 2026-06-21]]"
  - "[[sources/Horizon 每日速递 2026-06-22]]"
updated: 2026-06-22
---

# Horizon

开源 AI 新闻雷达。多源抓取 → AI 打分过滤 → 生成中英双语日报。

- 仓库：https://github.com/Thysrael/Horizon
- 语言：Python（uv 管理依赖）
- 部署：本地 / Docker / GitHub Actions

## Pipeline

```
Hacker News / Reddit / RSS / Telegram / Twitter / GitHub / OpenBB
    → 抓取
    → 去重
    → AI 打分（0-10，支持 Claude/GPT/Gemini/DeepSeek 等）
    → 背景补充（搜索补全陌生概念）
    → 评论总结
    → 分发（GitHub Pages / 邮件 / Webhook / MCP）
```

## 与 LLM Wiki 的关联

Horizon 本质上是 **[[LLM Wiki 模式]] 在新闻消费领域的应用**：LLM 做筛选、整理、归档的簿记工作，人类只消费最终产出。本知识库中的两篇日报就是它的产物。

## 关联连接
- [[MCP]]
- [[LLM Wiki 模式]]
- [[本地项目汇总]]
- [[GBrain]]
- [[Token Studio ROI]]
- [[Claude Code]]
- [[Benchmark vs 任务交付]]
- [[Codebase Memory MCP]]
- [[Headroom]]
