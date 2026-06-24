---
title: "GBrain"
type: entity
category: tool
tags:
  - entity
  - tool
  - llm
  - knowledge-management
  - memory
related:
  - "[[LLM Wiki 模式]]"
  - "[[Horizon]]"
  - "[[MCP]]"
  - "[[知识复利]]"
sources:
  - "[[wiki/entities/本地项目汇总|本地项目汇总]]"
updated: 2026-06-22
---

# GBrain

Garry Tan（YC 总裁）开源的 AI Agent 记忆系统。为 AI Agent 提供持久化、可搜索、自我改进的长期记忆。

- 仓库：https://github.com/garrytan/gbrain
- 本地：`D:\php_code\ai_project\gbrain-master`
- 星数：14K+
- 许可：MIT

## 核心能力

- **摄入**：会议、邮件、推文、通话、笔记 → Markdown 知识图谱
- **检索**：混合搜索（向量 + 关键词 + 知识图谱），Postgres + pgvector
- **合成**：带引用的回答 + "差距分析"（明确标注不知道什么）
- **Dream Cycle**：夜间自动补充实体、修复引用、整合记忆

## 架构

三层设计，与 [[LLM Wiki 模式]] 高度同构：

| GBrain 层 | LLM Wiki 层 |
|-----------|-------------|
| Brain Repo（Markdown + Git） | Wiki 层 |
| Hybrid Search（向量 + 关键词） | index.md + 搜索 |
| Skills Layer（Markdown 工作流） | Schema（CLAUDE.md） |

## 与本知识库的关联

GBrain 和我们的知识库是**同一模式的不同实例**——都是 LLM 驱动的持久化知识系统。但 GBrain 更偏向 Agent 的"记忆外挂"，我们更偏向人类的"第二大脑"。

- [[LLM Wiki 模式]] — 共同的理论基础
- [[Horizon]] — 同样拉取到本地的开源项目
- [[知识复利]] — GBrain 的 Dream Cycle 就是知识复利的自动化实现

## 关联连接
- [[LLM Wiki 模式]]
- [[Horizon]]
- [[MCP]]
- [[知识复利]]
- [[本地项目汇总]]
- [[Context Engineering]]
- [[Memex]]
- [[Andrej Karpathy]]
- [[Obsidian]]
- [[Token Studio ROI]]
