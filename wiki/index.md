# 知识库索引

> 内容导向的目录。每个页面一条记录，包含链接和一行摘要。按类别组织。每次 ingest 后更新。

## 总览

- [[wiki/overview|知识库总览]] — AI 编程工具与方法论的全局视图，综合所有来源的演进理解

## 源文件摘要

- [[wiki/sources/Loop Engineering 循环工程|Loop Engineering 循环工程]] — 从 Prompt Engineering 到 Loop Engineering 的 AI 编程范式演进，含 Claude Code/Codex/Cursor 三工具实战
- [[wiki/sources/CC Switch 接入国内模型|CC Switch 接入国内模型]] — 使用 CC Switch 将 Claude Code 和 Codex 切换到 DeepSeek 等国内大模型
- [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]] — Karpathy 提出的 LLM 驱动知识库构建模式，本知识库的理论基础
- [[wiki/sources/谷歌大咖出走分析|谷歌大咖出走分析]] — 谷歌一周内流失两位 AI 大咖，深层分析其 Agent 战略的组织架构灾难
- [[wiki/sources/Horizon 每日速递 2026-06-21|Horizon 2026-06-21]] — 每日科技资讯（Headroom、Codebase Memory MCP、Cloudflare 临时账户等）
- [[wiki/sources/Horizon 每日速递 2026-06-22|Horizon 2026-06-22]] — 每日科技资讯（开放权重模型、AI 网络安全技能、sqlite-utils 4.0 等）
- [[wiki/sources/Horizon 项目介绍|Horizon 项目介绍]] — 开源 AI 新闻雷达，LLM Wiki 模式在新闻领域的应用
- [[wiki/sources/Vibe Coding 常见问题和解决|Vibe Coding 常见问题]] — 鱼皮的 Vibe Coding 速查手册，涵盖概念、工具、技巧、项目全流程
- [[wiki/sources/CodeX Computer Use 修复|CodeX Computer Use 修复]] — Windows 下 CodeX 插件异常的排查修复方案
- [[wiki/sources/Horizon 每日速递 2026-06-23|Horizon 2026-06-23]] — Claude Code 思考有损、Oak VCS、提示注入角色混淆等
- [[wiki/sources/CC-Switch 智谱 GLM 教程|CC-Switch + 智谱 GLM 教程]] — Claude Code 国内使用的第三个模型方案
- [[wiki/sources/Token Studio ROI 项目详解|Token Studio ROI 详解]] — Ryan 的本地 AI 编程 ROI 复盘系统设计理念
- [[wiki/sources/B站视频转本地AI知识库！新手也能3分钟上手|B站视频转本地AI知识库！新手也能3分钟上手]] — MIP耀的 B站视频转知识库自动化工作流，解决 Web Clipper 无法抓取 B站内容的问题
- [[wiki/sources/6月23日 github热榜：涨⭐前十项目全解析|6月23日 github热榜：涨⭐前十项目全解析]] — 大雄AI实战对 GitHub 热榜前十项目的深度解析，揭示 AI 工作流工具的发展趋势
- [[wiki/sources/Horizon 每日速递 2026-06-24|Horizon 2026-06-24]] — Horizon 每日科技资讯，包含AI编码循环瓶颈讨论、AI安全突破、基础设施漏洞等重要技术趋势
- [[wiki/sources/Codex 录制回放功能评测|Codex 录制回放功能评测]] — Codex Record & Replay功能技术评测，分析录制回放工作流原理、适用场景和技术实现
- [[wiki/sources/AI大模型原理解析|AI大模型原理解析]] — 大语言模型核心原理的深度技术解析，涵盖生成机制、Transformer架构、训练流程、模型规模等内容
- [[wiki/sources/Horizon 每日速递 2026-06-25|Horizon 2026-06-25]] — OpenAI发布定制AI芯片Jalapeno，高通40亿美元收购Modular，AI硬件竞争加剧
- [[wiki/sources/Horizon 每日速递 2026-06-26|Horizon 2026-06-26]] — AI首次完整读取赫库兰尼姆卷轴，IBM发布亚1纳米芯片，苹果推出AI专用M7系列
- [[wiki/sources/9年IDEA用户卸载IDEA|9年IDEA用户卸载IDEA]] — AI编程对开发工具的影响分析，从IDEA到AI编程工具的演进
- [[wiki/sources/B站视频转本地AI知识库！新手也能3分钟上手|B站视频转本地AI知识库！新手也能3分钟上手]] — MIP耀的 B站视频转知识库自动化工作流，解决 Web Clipper 无法抓取 B站内容的问题

## 实体

### 工具
- [[wiki/entities/Bilibili Web Clipper|Bilibili Web Clipper]] — 专为 B站设计的浏览器扩展，实现视频内容向 Obsidian 的自动化转换
- [[wiki/entities/Local REST API|Local REST API]] — Obsidian 官方插件，提供本地笔记库的 RESTful API 接口
- [[wiki/entities/karpathy-llm-wiki-vault|karpathy-llm-wiki-vault]] — 基于 Karpathy LLM Wiki 理念的开源知识库模板项目
- [[wiki/entities/Claude Code|Claude Code]] — Anthropic 推出的终端 AI 编程工具，支持 /goal 和 /loop 命令
- [[wiki/entities/Codex|Codex]] — OpenAI 推出的 AI 编程工具，含 CLI 和桌面 APP 两种形态
- [[wiki/entities/CC Switch|CC Switch]] — 免费开源跨平台工具，统一管理多个 AI 编程工具的模型配置
- [[wiki/entities/Cursor|Cursor]] — AI 编程 IDE，目前无原生 Loop 命令但可通过提示词实现
- [[wiki/entities/Obsidian|Obsidian]] — 本地 Markdown 知识管理工具，LLM Wiki 的浏览器/IDE
- [[wiki/entities/Antigravity|Antigravity]] — 谷歌 AI Agent 开发平台，组织混乱导致失败的典型案例
- [[wiki/entities/Headroom|Headroom]] — LLM 输入压缩工具，减少 60-95% Token 消耗
- [[wiki/entities/Codebase Memory MCP|Codebase Memory MCP]] — 代码库知识图谱 MCP 服务器，亚毫秒查询
- [[wiki/entities/Horizon|Horizon]] — 开源 AI 新闻雷达，多源抓取 + AI 打分 + 双语日报
- [[wiki/entities/Windsurf|Windsurf]] — AI 编程 IDE，Cursor 竞品，Cascade 模式
- [[wiki/entities/Oak|Oak]] — AI Agent 专用版本控制系统，虚拟挂载+并行任务
- [[wiki/entities/GBrain|GBrain]] — Garry Tan（YC 总裁）开源的 AI Agent 记忆系统
- [[wiki/entities/Token Studio ROI|Token Studio ROI]] — 鱼皮的本地 AI 编程 Token ROI 复盘系统

### 项目
- [[wiki/entities/本地项目汇总|本地项目汇总]] — `D:\php_code\ai_project\` 下 5 个项目的统一索引
- [[wiki/entities/Loop Demo|Loop Demo]] — Loop Engineering 三工具实战演示项目

### 人物
- [[wiki/entities/大雄AI实战|大雄AI实战]] — 专注于GitHub项目解析和AI技术教程的内容创作者，以系统化方式分析热门开源项目
- [[wiki/entities/MIP耀|MIP耀]] — B站知识库技术教程创作者，专注于将视频内容转化为 AI 可理解的知识库
- [[wiki/entities/程序员鱼皮|程序员鱼皮]] — AI 编程领域博主，多篇教程作者
- [[wiki/entities/Boris Cherny|Boris Cherny]] — Claude Code 之父
- [[wiki/entities/Peter Steinberger|Peter Steinberger]] — OpenClaw 之父
- [[wiki/entities/Andrej Karpathy|Andrej Karpathy]] — LLM Wiki 方法论提出者，Tesla 前 AI 总监、OpenAI 创始成员
- [[wiki/entities/Vannevar Bush|Vannevar Bush]] — Memex 构想提出者（1945），LLM Wiki 的精神前身
- [[wiki/entities/Noam Shazeer|Noam Shazeer]] — Google DeepMind 前工程副总裁，2026.06 离职
- [[wiki/entities/John Jumper|John Jumper]] — AlphaFold 核心负责人，2026.06 离职

### 公司/组织
- [[wiki/entities/Anthropic|Anthropic]] — Claude 和 Claude Code 的开发商
- [[wiki/entities/OpenAI|OpenAI]] — Codex 和 GPT 系列的开发商
- [[wiki/entities/DeepSeek|DeepSeek]] — 国内大模型提供商，支持 Anthropic 兼容协议
- [[wiki/entities/Google DeepMind|Google DeepMind]] — 谷歌 AI 研究部门，Gemini 和 AlphaFold 的诞生地

## 概念

- [[wiki/concepts/Loop Engineering|Loop Engineering（循环工程）]] — 2026 年中新兴的 AI 编程范式，核心是自动循环 + 反馈闭环
- [[wiki/concepts/Prompt Engineering|Prompt Engineering（提示词工程）]] — 2022-2024 主流范式，关注如何通过对话让 AI 理解需求
- [[wiki/concepts/Context Engineering|Context Engineering（上下文工程）]] — 2025 范式，关注在对的时候把对的信息喂给 AI
- [[wiki/concepts/Harness Engineering|Harness Engineering（驾驭工程）]] — 2026 年初范式，给 AI 搭建靠谱的工作环境（工具+测试+约束）
- [[wiki/concepts/Overbaking|Overbaking（过度烘焙）]] — Loop 运行过久导致 AI 开始乱加功能、乱删测试的现象
- [[wiki/concepts/WorkTree|WorkTree（工作隔离）]] — 多个 Agent 并行工作时使用独立工作目录避免代码冲突
- [[wiki/concepts/MCP|MCP（Model Context Protocol）]] — 模型上下文协议，让 AI 连接外部工具和数据源
- [[wiki/concepts/LLM Wiki 模式|LLM Wiki 模式]] — Karpathy 提出的增量构建+持久化维护的知识库模式（本知识库的元方法论）
- [[wiki/concepts/Memex|Memex]] — Vannevar Bush 1945 年构想的个人知识存储设备，LLM Wiki 精神前身
- [[wiki/concepts/知识复利|知识复利]] — wiki 随每次摄入和查询而增值的核心机制
- [[wiki/concepts/Benchmark vs 任务交付|Benchmark vs 任务交付]] — Agent 产品的护城河不是刷榜，而是错误恢复+状态保存+人工接管
- [[wiki/concepts/Vibe Coding|Vibe Coding]] — 用自然语言描述需求让 AI 写代码的实践范式
- [[wiki/concepts/GitHub热榜|GitHub热榜]] — GitHub平台上根据星标增长速度排序的项目榜单，反映了开源社区的技术关注点和发展趋势
- [[wiki/concepts/AI工作流工具|AI工作流工具]] — 将AI能力融入完整工作流程的工具系统，实现了从单一AI功能向端到端工作流的转变
- [[wiki/concepts/开源超级智能体框架|开源超级智能体框架]] — 能够协调多个子智能体执行复杂任务的综合性AI框架系统，强调开源特性和复杂任务处理能力
- [[wiki/concepts/智能体技能|智能体技能]] — AI智能体所具备的具体能力集合，通过结构化技能定义实现智能化任务执行和持续进化
- [[wiki/concepts/代码库记忆|代码库记忆]] — 通过技术手段将代码库转化为AI可理解、可查询的知识结构，解决大型项目中代码理解的效率问题
- [[wiki/concepts/视频转知识库|视频转知识库]] — 将视频内容通过技术手段自动转化为结构化知识库的概念和方法论
- [[wiki/concepts/多媒体知识摄入|多媒体知识摄入]] — 将视频、音频、图像等多媒体内容转化为可检索、可分析、可关联的结构化知识
- [[wiki/concepts/AI幻觉|AI幻觉]] — AI 编造不存在内容的固有问题及应对方法
- [[wiki/concepts/录制回放工作流|录制回放工作流]] — 通过录制用户操作自动生成可复用工作流技能的新范式
- [[wiki/concepts/Transformer架构|Transformer架构]] — 现代大语言模型的基础架构，具有注意力机制和并行计算能力

## 对比

- [[wiki/comparisons/Claude Code vs Codex vs Cursor|Claude Code vs Codex vs Cursor]] — 三大 AI 编程工具的 Loop 能力对比
- [[wiki/comparisons/AI 编程四范式演进|AI 编程四范式演进]] — Prompt → Context → Harness → Loop 的层层递进关系

---

*索引更新时间：2026-06-22*
