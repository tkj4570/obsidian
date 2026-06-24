---
title: "CodeX Computer Use 插件修复"
type: source
source_url: "https://www.cnblogs.com/googlegis/p/20288340"
author: "googlegis"
published: 2026-06-03
ingested: 2026-06-23
tags:
  - source
  - ai-programming
  - codex
  - troubleshooting
related:
  - "[[Codex]]"
---

# CodeX Computer Use 插件修复

> Windows 下 CodeX 提示 "Computer Use plugins unavailable" 的完整排查修复方案。

## 核心内容

一套可直接丢给 CodeX 执行的 PowerShell 排查提示词，用于修复 Windows 文件锁导致的 bundled 插件半更新问题。覆盖：诊断、备份、重建 bundled marketplace、修复 Chrome/Computer Use 缓存、验证 4 个环节。

涉及：`EBUSY`、`plugin_cache_windows_file_lock`、`os error 5` 等关键错误关键词。
