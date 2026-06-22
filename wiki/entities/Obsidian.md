---
title: "Obsidian"
type: entity
category: tool
tags:
  - entity
  - tool
  - knowledge-management
related:
  - "[[LLM Wiki 模式]]"
  - "[[Dataview]]"
  - "[[Marp]]"
sources:
  - "[[sources/LLM Wiki 方法论]]"
updated: 2026-06-22
---

# Obsidian

基于本地 Markdown 文件的知识管理工具（"第二大脑"）。在 LLM Wiki 方法论中扮演 **Wiki 浏览器的角色**——Karpathy 的比喻："Obsidian 是 IDE，LLM 是程序员，wiki 是代码库。"

## 在 LLM Wiki 中的作用

- **图谱视图**：可视化 wiki 的连接结构——哪些页面是枢纽、哪些是孤儿
- **Wiki-link**：`[[双向链接]]` 是实现"交叉引用已就位"的关键机制
- **YAML Frontmatter**：配合 [[Dataview]] 实现动态查询

## 推荐配置（来自 Karpathy）

- 附件文件夹路径 → `raw/assets/`
- 绑定"下载当前文件附件"快捷键（Ctrl+Shift+D）
- 开启 Obsidian Web Clipper 浏览器扩展，快速剪藏网页文章

## 相关插件

- [[Dataview]]：对页面 Frontmatter 运行查询，生成动态表格
- [[Marp]]：Markdown 转幻灯片
- Excalidraw：画布/图表

## 在本知识库中

本知识库本身就是 Obsidian Vault + LLM 维护的 LLM Wiki 实例。
