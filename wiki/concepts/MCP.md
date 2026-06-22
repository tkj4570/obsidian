---
title: "MCP（Model Context Protocol）"
type: concept
tags:
  - concept
  - protocol
  - ai-programming
related:
  - "[[Loop Engineering]]"
  - "[[Harness Engineering]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# MCP（Model Context Protocol）

模型上下文协议。Loop Engineering 五大模块之一（工具连接）。让 AI 模型连接到外部工具和数据源的协议标准。

## 解决的问题

LLM 只是"大脑"——能思考、能规划，但如果不接上"手脚"和"工具"，很多事情干不了。

## 能力范围

通过 MCP 和各种连接器，Loop 可以：
- 连接 Issue 跟踪器（自动分类和处理 Issue）
- 连接数据库（查询和操作数据）
- 连接 Slack（发送通知）
- 连接 CI/CD 系统（查看报错日志）
- 自动开 PR 并发消息通知你

## 在 Loop 中的角色

有了 MCP 工具连接，Loop 才能从「只会改代码」变成「能发现问题、解决问题、通知你结果」的完整闭环。

同样属于进阶优化——基础循环跑起来之后再按需添加。
