---
title: "Context Engineering（上下文工程）"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Prompt Engineering]]"
  - "[[Harness Engineering]]"
  - "[[Loop Engineering]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# Context Engineering（上下文工程）

2025 年主流的 AI 编程范式。关注的是**怎么在对的时候把对的信息喂给 AI**。

## 核心方法

- 写 AGENTS.md / CLAUDE.md 规则文件让 AI 了解项目背景
- 用 RAG 让 AI 能检索到相关资料
- 给 AI 建立跨对话的记忆机制

## 解决的核心问题

「AI 给出的回答脱离实际」——光写好提示词不够，AI 还得了解你的项目背景才能给出靠谱回答。做好了上下文管理，AI 的输出才能贴合项目实际情况。

## 在演进中的位置

位于 Prompt Engineering 之上，Harness Engineering 之下。详见 [[comparisons/AI 编程四范式演进|AI 编程四范式演进]]。

## 与本知识库的关系

本知识库的 `CLAUDE.md` 就是 Context Engineering 的实践——它告诉 LLM 知识库的结构、规范和操作流程，让 LLM 能在正确理解上下文的基础上维护 wiki。
