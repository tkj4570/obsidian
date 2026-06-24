---
title: "AI幻觉"
type: concept
tags:
  - concept
  - llm
  - ai-programming
related:
  - "[[Vibe Coding]]"
  - "[[Overbaking]]"
sources:
  - "[[sources/Vibe Coding 常见问题和解决]]"
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-22
---

# AI幻觉（Hallucination）

AI 编造不存在的内容——虚构的 API、错误的函数用法、不存在的库。这是 LLM 基于概率生成内容的固有问题，不是 bug。

## 应对方法

1. **要求验证**：让 AI 提供文档链接，提供不了就说明是幻觉
2. **切断上下文**：如果 AI 陷入死循环，开新对话
3. **换个模型**：不同模型的幻觉倾向不同
4. **自己查文档**：养成查官方文档的习惯

## 与 Overbaking 的关联

[[Overbaking]] 可以看作是 AI 幻觉在循环中的放大版——Loop 跑太久，AI 开始"加戏"（乱加功能、删除测试），本质上也是在编造"看起来合理但实际不存在/不需要"的东西。

## 关联连接
- [[Vibe Coding]]
- [[Overbaking]]
- [[Context Engineering]]
- [[LLM Wiki 模式]]
- [[Benchmark vs 任务交付]]
- [[Claude Code]]
- [[Cursor]]
- [[Windsurf]]
