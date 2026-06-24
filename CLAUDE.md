# CLAUDE.md — 知识库维护大纲

本文件是 LLM 维护本知识库的核心规范。它告诉 LLM：知识库如何组织、页面应遵循什么格式、以及执行 ingest/query/lint 操作时应遵循什么流程。

---

## 一、三层架构

```
raw/               ← 原始资料层（只读，LLM 不修改）
  articles/        ← 博客文章、教程（含 Obsidian Web Clipper 输出）
  papers/          ← 学术论文、研究报告
  docs/            ← 官方文档
  books/           ← 书籍章节
  transcripts/     ← 视频/播客文字稿
wiki/              ← Wiki 层（LLM 全权维护）
  overview.md      ← 知识库总览 / 综合论述
  index.md         ← 内容目录（按类别列出所有页面 + 一行摘要）
  log.md           ← 操作日志（按时间追加，记录所有 ingest/query/lint）
  sources/         ← 源文件摘要页（每个原始资料对应一页）
  entities/        ← 实体页（工具、人物、公司、项目等）
  concepts/        ← 概念页（方法论、模式、术语等）
  comparisons/     ← 对比页（工具对比、方法论对比等）
CLAUDE.md          ← 本文件（Schema 层，与用户共同演进）
```

> **注意**：Obsidian Web Clipper 应配置为保存到 `raw/articles/` 目录，而非根目录的 `Clippings/`。

**原则**：
- `raw/` 及其子目录中的原始文件**不可修改**
- Wiki 层的所有 `.md` 文件由 LLM 创建和维护
- 用户负责策展来源、提出问题、审查更新；LLM 负责所有书写和簿记工作

---

## 二、页面规范

### 2.1 文件命名

- 使用**中文**命名（易于在 Obsidian 中浏览和搜索）
- 源摘要页：`sources/文章标题.md`
- 实体页：`entities/实体名.md`
- 概念页：`concepts/概念名.md`
- 对比页：`comparisons/对比主题.md`
- 文件名中避免特殊字符（`/ \ : * ? " < > |`）

### 2.2 YAML Frontmatter

每个 wiki 页面必须在顶部包含 YAML frontmatter。各类型页面的模板如下：

**源摘要页** (`sources/`)：
```yaml
---
title: "文章标题"
type: source
source_url: "原始链接"
author: "作者"
published: YYYY-MM-DD
ingested: YYYY-MM-DD
tags:
  - source
  - 主题标签
related:
  - "[[相关实体]]"
  - "[[相关概念]]"
---
```

**实体页** (`entities/`)：
```yaml
---
title: "实体名"
type: entity
category: tool | person | company | project
tags:
  - 标签
related:
  - "[[相关概念]]"
  - "[[相关实体]]"
sources:
  - "[[sources/来源文章]]"
updated: YYYY-MM-DD
---
```

**概念页** (`concepts/`)：
```yaml
---
title: "概念名"
type: concept
tags:
  - 标签
related:
  - "[[相关概念]]"
  - "[[相关实体]]"
sources:
  - "[[sources/来源文章]]"
updated: YYYY-MM-DD
---
```

**对比页** (`comparisons/`)：
```yaml
---
title: "对比主题"
type: comparison
tags:
  - comparison
related:
  - "[[实体A]]"
  - "[[实体B]]"
updated: YYYY-MM-DD
---
```

### 2.3 内部链接

- 始终使用 Obsidian Wiki-link 语法：`[[页面名]]` 或 `[[路径/页面名]]`
- 在页面正文中首次提及另一 wiki 页面时，使用 `[[Wiki-link]]`
- 引用源文件时，使用 `[[sources/文章标题|显示文字]]`
- **强制双向链接规则**：每个 wiki 页面必须包含 `## 关联连接` 区域，使用 `[[页面名称]]` 链接到其他相关概念，绝不能产生孤岛页面
- **矛盾处理原则**：如果新摄入的知识与旧知识冲突，不要静默覆盖。在页面中新建 `## 知识冲突` 区块，将两种说法都保留并做对比

### 2.4 标签体系

| 标签 | 用途 |
|------|------|
| `#source` | 标记源摘要页 |
| `#entity` | 标记实体页 |
| `#concept` | 标记概念页 |
| `#comparison` | 标记对比页 |
| `#overview` | 标记总览页 |
| `#ai-programming` | AI 编程相关 |
| `#tool` | 工具类内容 |
| `#methodology` | 方法论类内容 |
| `#llm` | 大语言模型相关 |
| `#claude-code` | Claude Code 相关 |
| `#codex` | Codex 相关 |
| `#cursor` | Cursor 相关 |

可根据需要添加新标签。

---

## 三、工作流

### 3.1 Ingest（摄入新来源）

当用户将新文件放入 `raw/articles/`（或其他 `raw/` 子目录）并请求处理时，执行以下步骤：

1. **读取源文件**：完整阅读源文件内容
2. **讨论要点**：与用户讨论关键发现，了解用户想强调什么
3. **创建源摘要页**：在 `wiki/sources/` 创建摘要页面，包含：
   - 文章的核心观点（3-5 条）
   - 关键引用（如有）
   - 涉及的新实体和新概念
4. **更新实体页**：为文章中提到的工具、人物、公司创建或更新 `wiki/entities/` 中的页面
5. **更新概念页**：为文章中涉及的方法论、术语创建或更新 `wiki/concepts/` 中的页面
6. **创建对比页**：如果文章涉及工具或方法论的对比，考虑创建 `wiki/comparisons/` 页面
7. **更新 overview.md**：如果新信息改变了全局理解，更新总览
8. **更新 index.md**：添加新页面的条目
9. **追加 log.md**：记录本次 ingest 操作
10. **强制双向链接**：确保每个新创建的页面都包含 `## 关联连接` 区域，链接到相关概念
11. **矛盾检查**：如果发现新知识与旧知识冲突，在页面中添加 `## 知识冲突` 区块，保留两种说法并做对比

一次 ingest 可能触及 5-15 个 wiki 页面。

### 3.2 Query（回答问题）

当用户提问时：

1. **先读 index.md**：定位相关页面
2. **深入阅读**：打开相关页面获取详细信息
3. **综合回答**：给出带 [[Wiki-link]] 引用的回答
4. **考虑归档**：如果回答本身有价值（对比、分析、洞察），询问用户是否要归档为新的 wiki 页面

### 3.3 Lint（健康检查）

当用户要求 lint 时，系统性地检查：

1. **矛盾检查**：不同页面是否存在互相矛盾的说法
2. **过时信息**：是否有被新来源取代的旧说法
3. **孤儿页面**：是否有没有任何入站链接的页面（overview/index/log 除外）
4. **缺失页面**：是否有重要概念被提及但缺少自己的页面
5. **断链**：是否有 Wiki-link 指向不存在的页面
6. **交叉引用缺失**：两个显然相关的页面是否缺少互相链接
7. **信息缺口**：是否有可以通过网络搜索填补的知识空白

输出一份结构化报告，提出具体的修复建议和新问题/新来源建议。

---

## 四、特殊文件规范

### 4.1 index.md 格式

```markdown
# 知识库索引

## 总览
- [[wiki/overview|知识库总览]] — 全局视角与综合论述

## 源文件摘要
- [[wiki/sources/文章标题|文章标题]] — 一行摘要描述

## 实体
- [[wiki/entities/实体名|实体名]] — 一行摘要描述

## 概念
- [[wiki/concepts/概念名|概念名]] — 一行摘要描述

## 对比
- [[wiki/comparisons/对比主题|对比主题]] — 一行摘要描述
```

每次 ingest 后必须更新。

### 4.2 log.md 格式

```markdown
# 操作日志

## [YYYY-MM-DD] ingest | 文章标题
- 创建源摘要页: [[wiki/sources/文章标题]]
- 创建/更新实体: [[wiki/entities/实体A]], [[wiki/entities/实体B]]
- 创建/更新概念: [[wiki/concepts/概念A]]
- 更新: [[wiki/index]], [[wiki/overview]]

## [YYYY-MM-DD] query | 问题简述
- 归档回答: [[wiki/pages/新页面]]（如有）

## [YYYY-MM-DD] lint
- 发现问题: ...
- 修复: ...
```

格式一致性很重要——这使得 `grep "^## \[" wiki/log.md | tail -10` 可以快速查看最近 10 条记录。

---

## 五、迭代原则

- 本 schema 是一份**活的文档**，随着知识库的演进而共同演进
- 用户和 LLM 应根据实际使用体验持续改进规范
- 如果某种页面格式不适用，修改它
- 如果某个工作流过于繁琐，简化它
- 如果缺少某种页面类型，添加它
- 所有约定都是可选的、可修改的——选择有用的，忽略无用的

---

## 六、当前知识库概况

- **领域**：AI 编程工具与方法论
- **语言**：中文（简体）
- **Obsidian 配置**：图片附件自动下载到本地
- **工作环境**：Obsidian + Claudian（LLM 助手）
- **模型**：DeepSeek V4 Pro（通过本地代理）
