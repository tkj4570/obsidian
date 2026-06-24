---
title: "把B站视频转成本地AI知识库！新手也能3分钟上手"
url: "https://www.bilibili.com/video/BV1g1dLBPEHV/"
bvid: "BV1g1dLBPEHV"
cid: "37589944385"
author: "MIP耀"
upload_date: "2026-04-18"
subtitle_lang: "中文"
created: "2026-06-24"
tags: ["clippings", "bilibili"]
---

<iframe src="https://player.bilibili.com/player.html?aid=116420927166252&bvid=BV1g1dLBPEHV&cid=37589944385&page=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allow="fullscreen; picture-in-picture" allowfullscreen="true" style="height:100%;width:100%; aspect-ratio: 16 / 9;"> </iframe>

##### B站视频转本地AI知识库指南.md

#### 📌 核心概念

- 将B站视频转化为本地AI可理解的知识库
- 解决B站视频无法被Obsidian原生Web Clipper抓取的问题
- 实现从视频收藏到知识生长的完整工作流

#### 🛠️ 工具链

|工具|功能|
|---|---|
|Obsidian|本地知识库核心，支持双链笔记与图谱可视化|
|Local REST API|提供读写笔记库的标准化接口|
|Bilibili Web Clipper|专为B站定制的抓取工具|

#### 📋 操作步骤

##### 1. 环境准备

- 克隆 [karpathy-llm-wiki-vault](https://github.com/jason-effi-lab/karpathy-llm-wiki-vault) 仓库到本地
- 在Obsidian中打开该仓库

##### 2. 插件安装

- 在Obsidian中安装Local REST API插件
- 打开插件选项，复制API key
- 启用HTTP服务器选项

##### 3. 浏览器扩展配置

- 安装Bilibili Web Clipper浏览器扩展（支持Chrome、Edge、Firefox）
- 打开任意B站视频页面
- 点击扩展图标进行首次配置
- 粘贴API key
- 设置笔记目录为 `raw/03transcripts`

##### 4. 视频入库

- 打开B站学习视频
- 点击浏览器右上角的插件图标
- 点击"保存至Obsidian"
- 插件自动提取标题、UP主、字幕和简介，生成markdown文件

##### 5. 知识处理

- 使用Obsidian的技能功能（如injs query.lt）处理笔记
- 自动完成双向链接与知识图谱构建
- 原文件自动归档，生成概念实体和摘要

#### 💡 解决方案

- **平台差异**：B站采用不同播放器与页面结构，通过专用插件解决
- **字幕格式**：B站字幕格式特殊，需要专门解析
- **特有数据**：B站特有的B站数据通过插件单独处理

#### 🔗 相关资源

- 原知识库仓库：https://github.com/jason-effi-lab/karpathy-llm-wiki-vault
- B站视频插件仓库：https://github.com/haixiong1997/Bilibili-Obsidian-Clipper

---

#### 写入Obsidian的方法：

1. **手动创建文件**：

- 在Obsidian的`raw/03transcripts`目录下创建新文件
- 将上述内容复制粘贴到新文件中
- 保存并命名为"B站视频转本地AI知识库指南.md"

2. **使用模板插件**：

- 安装Templater或QuickAdd插件
- 创建知识库模板
- 使用模板自动生成格式化的文档

3. **通过Local REST API**：

- 使用API直接向Obsidian写入文件
- 可以编写脚本批量处理多个文档

4. **拖拽导入**：

- 将.md文件直接拖拽到Obsidian库中
- Obsidian会自动识别并建立链接