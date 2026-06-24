---
title: "Loop Engineering（循环工程）"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Prompt Engineering]]"
  - "[[Context Engineering]]"
  - "[[Harness Engineering]]"
  - "[[Overbaking]]"
  - "[[WorkTree]]"
  - "[[MCP]]"
  - "[[Claude Code]]"
  - "[[Codex]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# Loop Engineering（循环工程）

2026 年中新兴的 AI 编程范式。核心思想：从手动一句一句提示 AI，转变为设计一套自动循环系统来驱动 AI 工作。

## 类比

- **旧模式 = 手动挡汽车**：每一步都要你操作。你给 AI 一句提示词，AI 回一段代码，停下等你下一条指令。
- **Loop 模式 = 自动驾驶**：设定目的地和安全规则，车自己开。你把"提示、检查、决定下一步"交给系统，自己只设定目标。

角色转变：从 AI 的"操作者"变为循环规则的"设计者/管理者"。

## 三要素

1. **明确的目标和停止条件**（可验证的）
   - 好的：所有测试通过、lint 零报错、所有文件都处理完
   - 坏的：「把代码优化一下」（无法验证什么叫优化好）
   
2. **反馈闭环**
   - 每轮循环结束后检查结果，判断继续还是停止
   - 常见做法：跑完代码后自动执行测试

3. **状态记忆**
   - 外部文件记录进度（如 PROGRESS.md）
   - 中间断了重启不会从零开始

## 五大核心模块

除了三要素，更完整的 Loop 系统包含：

1. **自动调度**：Loop 的心跳，按设定的条件和频率运行
2. **工作隔离（WorkTree）**：多 Agent 并行时用独立工作目录避免冲突
3. **技能沉淀（Skills）**：可复用的 SKILL.md 文档，Loop 启动时自动加载
4. **工具连接（MCP）**：通过 MCP 协议连接 Issue 跟踪器、数据库、CI/CD 等
5. **子代理互审**：不同 Agent 分别负责编写和审查，避免"自己审自己"的偏差

## 在 AI 编程演进中的位置

```
Prompt Engineering → Context Engineering → Harness Engineering → Loop Engineering
        (基础)              (基础)               (基础)                (当前前沿)
```

Loop 不是取代前三个，而是建立在前三个基础上加了一层"自动循环 + 反馈闭环"。详见 [[comparisons/AI 编程四范式演进|AI 编程四范式演进]]。

## 注意事项

- **Token 消耗大**：每次迭代都是一次完整调用，高频循环 = 高昂成本
- **调试困难**：跑了 47 轮的状态机很难追溯哪轮出了问题
- **[[Overbaking]] 过度烘焙**：跑太久 AI 可能乱加功能、乱删测试
- **建议**：从 `/goal` 轻量方式开始，设小目标，熟了再加复杂度

## 相关人物

- [[Boris Cherny]] — Claude Code 之父，最早倡导者
- [[Peter Steinberger]] — OpenClaw 之父，同期倡导者

## 关联连接
- [[Prompt Engineering]]
- [[Context Engineering]]
- [[Harness Engineering]]
- [[Overbaking]]
- [[WorkTree]]
- [[MCP]]
- [[Claude Code]]
- [[Codex]]
- [[Benchmark vs 任务交付]]
- [[Vibe Coding]]
- [[AI幻觉]]
- [[知识复利]]
