---
title: "LLM Wiki 方法论"
type: source
source_url: "原始 Gist（作者 Andrej Karpathy）"
author: "[[Andrej Karpathy]]"
published: 2026-06
ingested: 2026-06-22
tags:
  - source
  - methodology
  - knowledge-management
  - llm
related:
  - "[[LLM Wiki 模式]]"
  - "[[Memex]]"
  - "[[知识复利]]"
  - "[[Obsidian]]"
  - "[[Andrej Karpathy]]"
---

# LLM Wiki 方法论

> 来源：Andrej Karpathy，2026.06 | 理念文档（idea file）

## 核心观点

1. **RAG 的局限**：传统 RAG 每次查询从零检索、拼凑片段，知识无法积累。LLM Wiki 的核心洞察是**让 LLM 增量构建持久化的知识产物**——编译一次，持续保鲜，而非每次重新推导。

2. **Wiki 是"复利产物"**：交叉引用已就位、矛盾已标记、综合论述已反映所有已读内容。每加一个资料、每问一个问题，wiki 都更丰富。知识不会消失在聊天记录中。

3. **三层架构**：
   - **原始资料**：用户策展，LLM 只读不写
   - **Wiki**：LLM 全权维护的 Markdown 集合
   - **Schema**：与用户共同演进的规范文件（如 [[CLAUDE.md]]）

4. **三个操作**：
   - **Ingest**：读资料 → 讨论要点 → 写摘要 → 更新实体/概念页 → 更新索引 → 记日志。一次可能触及 10-15 个页面。
   - **Query**：查 wiki → 综合回答 → **好答案归档回 wiki**（关键！）
   - **Lint**：扫矛盾、扫孤儿页、扫过时信息、扫缺失交叉引用

5. **Observable 是 IDE，LLM 是程序员，Wiki 是代码库**——这是 Karpathy 的实践隐喻。

## 关键引用

> "wiki 是一个持久化的、不断复利的产物。交叉引用已经就位，矛盾已经被标记，综合论述已经反映了你读过的一切。"

> "你几乎从不自己写 wiki——LLM 编写和维护所有内容。你负责策展来源、探索和提出正确的问题。"

> "Obsidian 是 IDE，LLM 是程序员，wiki 是代码库。"

## 知识库场景

Karpathy 列举了 LLM Wiki 适用的六大场景：
- **个人**：目标、健康、心理追踪
- **研究**：数周到数月的深度主题研究
- **读书**：逐章构建角色/主题/情节 wiki
- **商业/团队**：Slack + 会议 + 文档驱动的内部 wiki
- **竞品分析、尽职调查、旅行规划、课程笔记、兴趣深耕**

## 涉及的新概念

- [[LLM Wiki 模式]] — 本篇描述的核心方法论
- [[Memex]] — Vannevar Bush 1945 年的构想，LLM Wiki 的精神前身
- [[知识复利]] — wiki 随每次摄入和查询而增值的核心机制

## 涉及的工具/实体

- [[Andrej Karpathy]] — 作者，Tesla 前 AI 总监、OpenAI 创始成员
- [[Obsidian]] — 推荐的知识库浏览工具
- [[Vannevar Bush]] — Memex 提出者
- [[Marp]] — Markdown 幻灯片工具
- [[Dataview]] — Obsidian 动态查询插件
- [[qmd]] — 本地 Markdown 搜索引擎

## 与已有知识的关联

本篇是本知识库的**元方法论**来源——我们的 [[CLAUDE.md]]、三层架构、Ingest/Query/Lint 工作流、[[wiki/index|索引]]和[[wiki/log|日志]]结构，全部直接源自这篇文章的设计。

它和 [[sources/Loop Engineering 循环工程|Loop Engineering]] 文章形成有趣对照：Loop Engineering 讲的是"让 LLM 写代码时自动循环"，LLM Wiki 讲的是"让 LLM 维护知识时不断复利"——核心思想相通：**让 LLM 做持续的簿记工作，人类做策展和思考。**
