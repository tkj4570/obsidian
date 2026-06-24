---
title: "Vibe Coding"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Prompt Engineering]]"
  - "[[Context Engineering]]"
  - "[[AI幻觉]]"
  - "[[Cursor]]"
  - "[[Claude Code]]"
sources:
  - "[[sources/Vibe Coding 常见问题和解决]]"
updated: 2026-06-22
---

# Vibe Coding

用自然语言描述需求，让 AI 帮你写代码的编程范式。

## 类比

- **传统编程 = 自己做饭**：掌握语法、细节、工具，全程手动
- **Vibe Coding = 点外卖**：描述你想吃什么，等 AI 做好端上来

## 适用场景

| 适合 | 不适合 |
|------|--------|
| 快速原型开发 | 极复杂系统 |
| 个人项目 | 对性能极致要求的场景 |
| 中小型应用 | 需要深度底层优化的项目 |
| 工具类软件 | — |

## 在 AI 编程演进中的位置

Vibe Coding 不是一个独立范式，而是 **Prompt Engineering + Context Engineering + Harness Engineering 的实践总和**：

- 写好的提示词 → [[Prompt Engineering]]
- 配置 `.cursorrules` / `CLAUDE.md` → [[Context Engineering]]
- 搭测试、做重构、用 Git → [[Harness Engineering]]

Vibe Coding 是这些范式的"用户体验层"——降低入门门槛，让更多人能用 AI 编程。

## 核心原则

1. **从小做起（MVP）**：先做能跑的最简版本，再迭代
2. **不要盲目信任 AI**：测试、审查、验证
3. **提示词越具体越好**：功能 + 界面 + 技术 + 参考
4. **Git 是救命稻草**：频繁提交，随时可回退
5. **遇到问题换模型**：不要死磕一个 AI，不同模型擅长的领域不同

## 关联连接
- [[Prompt Engineering]]
- [[Context Engineering]]
- [[AI幻觉]]
- [[Cursor]]
- [[Claude Code]]
- [[Windsurf]]
- [[Overbaking]]
- [[Loop Engineering]]
- [[LLM Wiki 模式]]
