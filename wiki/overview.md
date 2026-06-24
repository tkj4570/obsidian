---
title: "知识库总览"
type: overview
tags:
  - overview
  - ai-programming
updated: 2026-06-22
---

# AI 编程工具与方法论 — 知识库总览

## 本知识库是什么

这是一个关于 **AI 编程工具与方法论** 的个人知识库。它由 LLM 增量构建和维护，基于用户策展的原始资料，持续积累对 AI 编程领域的理解。

**本知识库本身是 LLM Wiki 模式的一个实例**——它的架构、工作流和演进方式直接遵循 [[Andrej Karpathy]] 的 [[LLM Wiki 模式|LLM Wiki 方法论]]。详见 [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]]。

核心关注点：
- **AI 编程工具**：Claude Code、Codex、Cursor 等工具的原理、用法和对比
- **AI 编程范式**：从 Prompt Engineering 到 Loop Engineering 的演进历程
- **知识管理方法**：LLM Wiki 模式、知识复利机制、Schema 共演进
- **实用技巧**：模型切换、配置优化、工作流设计

## 当前知识结构

### AI 编程范式的演进

```
Prompt Engineering (2022-2024)
    ↓ 关注「如何让 AI 理解需求」
Context Engineering (2025)
    ↓ 关注「如何在对的时候给 AI 对的上下文」
Harness Engineering (2026初)
    ↓ 关注「如何给 AI 搭建靠谱工作环境」
Loop Engineering (2026中)
    ↓ 关注「如何让 AI 自己形成工作循环」
```

这是 AI 编程领域最核心的叙事线——从"手动挡"到"自动驾驶"的进化。详见 [[wiki/comparisons/AI 编程四范式演进|AI 编程四范式演进]]。

### 当前局面

截至 2026 年 6 月，Loop Engineering 是一个**早期概念**，业界尚无统一标准。两家头部公司（Anthropic 和 OpenAI）的工程师都在倡导这一方向，但最佳实践仍在探索中。

三大 AI 编程工具的 Loop 支持状态：
- [[wiki/entities/Claude Code|Claude Code]]：内置 `/goal` 和 `/loop`，最成熟
- [[wiki/entities/Codex|Codex]]：内置 `/目标` 和 Automations，需开启本地路由才能接国内模型
- [[wiki/entities/Cursor|Cursor]]：无原生支持，可通过提示词设计实现

### 已确认的关键洞察

1. **Loop 不是取代提示词的**——它是建立在提示词、上下文、Harness 之上的更高层抽象（四者层层包含）

2. **Loop 三要素**：明确目标+停止条件、反馈闭环、状态记忆——这三样缺一不可

3. **Token 成本是真实约束**——高频循环的 token 消耗不可忽视，需要在实际价值和成本间权衡

4. **Overbaking 是真实风险**——Loop 跑太久会开始"加戏"，需要合理的循环次数上限

5. **基础不牢，Loop 只是放大问题**——先打好 Prompt/Context/Harness 的基础再上 Loop

6. **知识复利是实现长期价值的关键**——LLM Wiki 和 Loop Engineering 共享同一底层逻辑：让 LLM 做簿记，让每次交互的产出持久积累而非消失在聊天记录中

7. **多媒体知识管理是 LLM Wiki 的自然延伸**——从文本知识到视频、音频等媒体内容的结构化处理，让知识体系更加立体和完整

8. **工具链整合是实用落地的关键**——专用工具（如 Bilibili Web Clipper）+通用工具（如 Local REST API）的组合实现端到端的自动化工作流

### 跨领域连接

- **LLM Wiki ↔ Loop Engineering**：两个看似不相关的概念共享核心思想——LLM 做持续的簿记工作，人类做策展和决策。详见 [[知识复利]]。

- **Antigravity 失败 ↔ Loop 三要素缺失**：谷歌 [[Antigravity]] 的失败恰好从反面验证了 [[Loop Engineering]] 的必要性——缺乏错误恢复、状态保存、人工接管等 Loop 机制，单步正确率再高的模型也无法可靠交付多步任务。详见 [[Benchmark vs 任务交付]]。

- **多媒体摄入 ↔ LLM Wiki**：[[视频转知识库]] 和 [[多媒体知识摄入]] 扩展了 LLM Wiki 的边界，将非文本内容纳入知识管理体系，体现了三层架构的适应性。

- **工具链整合 ↔ 实用价值**：[[Bilibili Web Clipper]] + [[Local REST API]] + [[Obsidian]] 的组合体现了从理论到实践的转化，降低了技术使用门槛。

- **GitHub热榜 ↔ AI工作流工具**：[[GitHub热榜]] 反映了 [[AI工作流工具]] 的兴起，揭示了从agent skills到agency agents再到product process AI的发展趋势，体现了AI工具的演进路径。

- **代码库记忆 ↔ AI编程效率**：[[代码库记忆]] 解决了AI编程中大型代码库理解效率低的核心痛点，是AI编程工具的关键基础设施。

- **智能体技能 ↔ 多智能体协作**：[[智能体技能]] 是 [[开源超级智能体框架]] 的基础，通过结构化技能定义实现了复杂任务的协作执行。

### 待探索的方向

- Loop Engineering 的最佳实践和设计模式
- 多个 Agent 并行协作的 WorkTree 隔离策略（已有概念，缺乏实战）
- MCP 协议在 AI 编程工具连接中的实际应用
- 国内模型（DeepSeek、Qwen 等）在 AI 编程场景中的表现对比
- 不同工具的 Skills/技能沉淀机制对比
- 多媒体内容的语义理解和自动关联机制
- 跨平台多媒体内容摄入的标准化流程
- 知识库中多媒体内容的高效检索和组织方式
- GitHub 热榜项目的深度分析和价值评估体系
- AI 工作流工具在实际项目中的应用效果和ROI分析
- 开源超级智能体框架的规模化部署和运维策略
- 智能体技能的标准化和跨平台兼容性

### 来源清单

当前知识库基于以下原始资料构建：

1. [[wiki/sources/Loop Engineering 循环工程|Loop Engineering 循环工程]] — 鱼皮，2026.06
2. [[wiki/sources/CC Switch 接入国内模型|CC Switch 接入国内模型]] — 鱼皮，2026.06
3. [[wiki/sources/LLM Wiki 方法论|LLM Wiki 方法论]] — Andrej Karpathy，2026.06（本知识库的元方法论）
4. [[wiki/sources/谷歌大咖出走分析|谷歌大咖出走分析]] — 字母AI，2026.06
5. [[wiki/sources/Horizon 每日速递 2026-06-21|Horizon 2026-06-21]] / [[wiki/sources/Horizon 每日速递 2026-06-22|2026-06-22]] — 每日科技资讯
6. [[wiki/sources/B站视频转本地AI知识库！新手也能3分钟上手|B站视频转本地AI知识库！新手也能3分钟上手]] — MIP耀，2026.04（多媒体知识摄入技术体系）
7. [[wiki/sources/6月23日 github热榜：涨⭐前十项目全解析|6月23日 github热榜：涨⭐前十项目全解析]] — 大雄AI实战，2026.06（GitHub热榜分析框架和AI工作流工具发展趋势）

---

*本页面是所有 ingest 和 query 的综合产物，随新来源的加入和新问题的探索持续演进。*
