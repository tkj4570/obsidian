---
title: "Antigravity"
type: entity
category: tool
tags:
  - entity
  - tool
  - ai-programming
  - google
related:
  - "[[Google DeepMind]]"
  - "[[Gemini]]"
  - "[[Claude Code]]"
  - "[[Codex]]"
  - "[[Benchmark vs 任务交付]]"
sources:
  - "[[sources/谷歌大咖出走分析]]"
updated: 2026-06-22
---

# Antigravity

谷歌的 AI Agent 开发平台，2025 年 11 月随 Gemini 3 首次发布（"agent-first"），2026 年 5 月 I/O 大会发布 2.0。当前是**反面教材级案例**。

## 产品形态（2.0）

分五层：桌面 App、CLI、SDK、Managed Agents、企业层。但 2.0 发布一个多月后仍无企业定价。

## 核心失败原因

1. **缺乏 Loop 机制**：没有类似 Claude Code `/goal` 的错误恢复、状态保存、人工接管能力
2. **组织归属混乱**：从 DeepMind 走出 → 归 Labs 维护 → 须接入 Cloud 体系 → 无人最终负责
3. **谷歌内部产品内耗**：与 Gemini CLI、Jules、Code Assist、Firebase Studio 五个产品功能重叠

## 与竞品对比

| 维度 | Antigravity 2.0 | Claude Code | Codex |
|------|----------------|-------------|-------|
| Loop 支持 | ❌ 无完整机制 | ✅ `/goal` + `/loop` | ✅ `/目标` + Automations |
| 企业定价 | 无 | Team 按人头 | Business/Enterprise |
| 社区口碑 | 骂声一片 | 高度认可 | 快速增长 |
| 年化收入 | 未商业化 | $20亿+ | 快速增长中 |

## 参见

- [[Benchmark vs 任务交付]] — Antigravity 失败的理论解释

## 关联连接
- [[Google DeepMind]]
- [[Gemini]]
- [[Claude Code]]
- [[Codex]]
- [[Benchmark vs 任务交付]]
- [[Overbaking]]
- [[Loop Engineering]]
- [[Harness Engineering]]
- [[Noam Shazeer]]
- [[John Jumper]]
