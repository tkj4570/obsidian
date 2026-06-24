---
title: "LLM Wiki 模式"
type: concept
tags:
  - concept
  - methodology
  - knowledge-management
  - llm
related:
  - "[[知识复利]]"
  - "[[Memex]]"
  - "[[Andrej Karpathy]]"
  - "[[Obsidian]]"
sources:
  - "[[sources/LLM Wiki 方法论]]"
updated: 2026-06-22
---

# LLM Wiki 模式

由 [[Andrej Karpathy]] 在 2026 年提出的知识库构建模式。核心主张：**LLM 增量构建并维护持久化 wiki，而非每次查询从零 RAG 检索**。

## 与传统 RAG 的本质区别

| 维度 | 传统 RAG | LLM Wiki |
|------|---------|----------|
| 知识状态 | 每次重新推导 | 编译一次，持续保鲜 |
| 交叉引用 | 查询时临时拼凑 | 预先建立，随增量更新 |
| 矛盾处理 | 不处理（可能给矛盾答案） | 主动标注、对比 |
| 知识积累 | 无 | 每次摄入+查询都在复利 |
| 维护者 | — | LLM 全权维护 |

## 三层架构

1. **原始资料层**：用户策展的文件集合，LLM 只读
2. **Wiki 层**：LLM 生成和维护的 Markdown 网络
3. **Schema 层**：与用户共同演进的规范文档

详见本知识库的 [[CLAUDE.md]]（我们的 Schema 实例）。

## 三个核心操作

- **Ingest**：读源 → 写摘要 → 更新实体 → 更新概念 → 更新索引 → 记日志
- **Query**：查 wiki → 综合回答 → 好答案归档回 wiki
- **Lint**：扫矛盾、扫孤儿页、扫过时信息、扫缺失链接

## 为什么行得通

维护知识库最难的不是阅读或思考——是**簿记**。LLM 不会无聊、不会忘记更新交叉引用、一次能触及 15 个文件。维护成本趋近于零。

人类的独特价值：策展来源、指导分析、提出好问题、思考意义。

## 精神前身

Vannevar Bush 的 [[Memex]]（1945）构想了同样的东西——私人策展的、带联想路径的知识存储。Bush 没解决"谁做维护"，LLM 解决了。

## 参见

- [[知识复利]] — wiki 增值的核心机制
- [[Memex]] — 历史渊源
- [[sources/LLM Wiki 方法论|LLM Wiki 方法论]] — 原始文章摘要

## 关联连接
- [[知识复利]]
- [[Memex]]
- [[Andrej Karpathy]]
- [[Obsidian]]
- [[CLAUDE.md]]
- [[Context Engineering]]
- [[Vibe Coding]]
- [[Benchmark vs 任务交付]]
