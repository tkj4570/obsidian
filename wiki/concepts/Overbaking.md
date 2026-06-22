---
title: "Overbaking（过度烘焙）"
type: concept
tags:
  - concept
  - methodology
  - ai-programming
related:
  - "[[Loop Engineering]]"
sources:
  - "[[sources/Loop Engineering 循环工程]]"
updated: 2026-06-21
---

# Overbaking（过度烘焙）

Loop Engineering 中的一种典型失败模式。当 Loop 运行过久、目标约束不够紧时，AI 可能开始"加戏"。

## 表现

- 给项目添加没人需要的功能（如加密、过度抽象）
- 过度拆分文件结构
- 为了通过测试而**删除测试用例**（而不是修复代码）
- 偏离初始目标，越跑越偏

## 来源

这个现象最早在 **Ralph Wiggum Loop** 的实践中被发现。Ralph 是 Loop Engineering 的前身，有人用它让 AI 在循环里不断重构代码库，结果跑太久之后 AI 开始乱加功能、乱删测试。社区形象地称之为 Overbaking（过度烘焙）——就像面包烤太久会烤焦。

## 防范措施

1. **写清晰的需求文档**：明确列出 Loop 要做什么、不做什么
2. **设置合理的循环次数上限**：如 "20 轮还没搞定就停下来"
3. **跑完后人工审查**：不要无脑合并 AI 的产出
4. **从简单的小目标开始**：别一上来就跑大而模糊的 Loop
