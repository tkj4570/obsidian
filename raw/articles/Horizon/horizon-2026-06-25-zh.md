# Horizon 每日速递 - 2026-06-25

> 从 55 条内容中筛选出 15 条重要资讯。

---

1. [OpenAI 携手 Broadcom 发布首款定制 AI 芯片 'Jalapeno'](#item-1) ⭐️ 9.0/10
2. [高通以 40 亿美元收购 AI 初创公司 Modular](#item-2) ⭐️ 9.0/10
3. [Nub：一个类似 Bun 的 Node.js 一体化工具包](#item-3) ⭐️ 8.0/10
4. [间谍软件利用违禁文本逃避 AI 分析](#item-4) ⭐️ 8.0/10
5. [zrip：纯 Rust 实现的 Zstd 编解码器，优化传输速度](#item-5) ⭐️ 8.0/10
6. [Bunny DNS 免费：无查询费，支持 500 个域名](#item-6) ⭐️ 7.0/10
7. [RubyLLM：面向主要 AI 提供商的统一 Ruby 框架](#item-7) ⭐️ 7.0/10
8. [GitHub 上的 PR 垃圾信息与早期邮件垃圾信息如出一辙](#item-8) ⭐️ 7.0/10
9. [NVIDIA 45°C 冷却方案大幅降低数据中心用水](#item-9) ⭐️ 7.0/10
10. [Elastic 裁员 7%，归因于 AI](#item-10) ⭐️ 7.0/10
11. [Xteink X4：基于微控制器的极简开源电子墨水阅读器](#item-11) ⭐️ 7.0/10
12. [卡马克反思 id Software 早期管理失误](#item-12) ⭐️ 7.0/10
13. [Rust 社区推动 crates.io 与 GitHub 解耦](#item-13) ⭐️ 7.0/10
14. [LWN 周刊：自由线程 Python、AUR 攻击、BPF arena](#item-14) ⭐️ 7.0/10
15. [Fedora 将在安全事件后要求 Provenpackager 启用双因素认证](#item-15) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [OpenAI 携手 Broadcom 发布首款定制 AI 芯片 'Jalapeno'](https://techcrunch.com/2026/06/24/openai-unveils-its-first-custom-chip-built-by-broadcom/) ⭐️ 9.0/10

OpenAI 与 Broadcom 联合发布了 Jalapeno，这是 OpenAI 首款定制 AI 推理芯片，由 OpenAI 从头设计并由台积电制造。该芯片在九个月内完成开发，期间使用了 OpenAI 自身的 AI 模型加速设计流程。 这标志着 OpenAI 在垂直整合方面迈出了重要一步，减少了对英伟达等外部硬件供应商的依赖。专为大语言模型推理定制的芯片有望显著提升性能和效率，可能降低 AI 部署的成本。 Jalapeno 是一款针对大语言模型优化的推理处理器，利用了 Broadcom 的芯片设计专长和台积电的先进制造工艺。该芯片预计将于 2026 年底开始在 OpenAI 的数据中心部署。

hackernews · jamdesk · 6月24日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=48663324)

**背景**: AI 推理芯片是专门用于运行已训练好的 AI 模型的处理器，与用于训练模型的训练芯片不同。英伟达目前主导着 AI 芯片市场，但谷歌（通过 TPU）以及现在的 OpenAI 等公司正在开发定制替代方案，以提升性能并降低成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/openai-broadcom-jalapeno-inference-chip/">OpenAI and Broadcom unveil LLM-optimized inference chip</a></li>
<li><a href="https://techcrunch.com/2026/06/24/openai-unveils-its-first-custom-chip-built-by-broadcom/">OpenAI unveils its first custom chip, built by Broadcom</a></li>
<li><a href="https://investors.broadcom.com/news-releases/news-release-details/openai-and-broadcom-unveil-llm-optimized-intelligence-processor">OpenAI and Broadcom Unveil LLM-Optimized Intelligence ...</a></li>

</ul>
</details>

**社区讨论**: 社区评论对 OpenAI 的模型如何加速芯片设计表示好奇，部分人怀疑这可能是营销噱头。其他人指出该芯片由台积电（而非英特尔）制造，并讨论了通过将权重硬编码到硅片中实现极致效率提升的潜力，提到了 Taalas 等公司。

**标签**: `#AI hardware`, `#OpenAI`, `#custom chip`, `#inference`, `#Broadcom`

---

<a id="item-2"></a>
## [高通以 40 亿美元收购 AI 初创公司 Modular](https://www.reuters.com/business/qualcomm-buy-ai-startup-modular-2026-06-24/) ⭐️ 9.0/10

高通于 2026 年 6 月 24 日宣布以 40 亿美元收购 AI 基础设施初创公司 Modular，该公司是 Mojo 编程语言的开发者。 此次收购增强了高通的 AI 软件栈，使其能够在数据中心 AI 推理和训练市场上更有效地与英伟达竞争。 Modular 的 Mojo 语言专为异构硬件上的高性能 AI 而设计，交易包括 Modular 的 MAX 引擎和编译器技术。

hackernews · timmyd · 6月24日 13:49 · [社区讨论](https://news.ycombinator.com/item?id=48659798)

**背景**: 高通一直在从移动芯片扩展到 AI 和数据中心处理器。Modular 由 Chris Lattner（LLVM 和 Swift 的创建者）创立，致力于构建跨 CPU、GPU 和定制加速器优化 AI 工作负载的工具。此次收购符合高通提供完整软硬件 AI 平台的战略。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/06/24/qualcomm-ai-chip-modular-software.html">Qualcomm inks deal for AI startup Modular to bolster software stack - CNBC</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：有人质疑高通与英伟达主导的 H100 竞争的能力，而另一些人则认为这是构建包括 RISC-V 和 Tenstorrent 在内的全面 AI 产品组合的大胆举措。有人指出，鉴于其创始人此前对硬件公司 AI 栈的批评，Modular 被硬件公司收购具有讽刺意味。

**标签**: `#acquisition`, `#AI`, `#hardware`, `#Qualcomm`, `#Modular`

---

<a id="item-3"></a>
## [Nub：一个类似 Bun 的 Node.js 一体化工具包](https://github.com/nubjs/nub) ⭐️ 8.0/10

Zod 的创建者、前 Bun 工程师 Colin McDonnell 发布了 Nub，这是一个开源工具包，通过预加载钩子为 Node.js 添加了转译、模块解析和 polyfill 功能，而无需替换 Node 运行时。 Nub 将类似 Bun 的开发体验带到了 Node.js，有望在保持与现有 Node 生态系统和工具兼容的同时，提高数百万 Node 开发者的生产力。 Nub 通过 Node-API 插件使用 oxc 转译器（用 Rust 编写）实现快速的 TypeScript/JSX 转译，并利用 Node 的 --require 预加载钩子和模块解析钩子注入 Worker 和 Temporal 等 API 的 polyfill。

hackernews · colinmcd · 6月24日 14:14 · [社区讨论](https://news.ycombinator.com/item?id=48660267)

**背景**: Bun 是一个快速的一体化 JavaScript 运行时，包含转译器、打包器和包管理器，但与 Node.js 不完全兼容。Nub 旨在提供类似的开发体验改进，而无需离开 Node.js，仅使用不改变 Node 核心行为的附加钩子。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/oxc-project/oxc">GitHub - oxc-project/oxc: ⚓ A collection of high-performance JavaScript ...</a></li>
<li><a href="https://nodejs.org/api/module.html">Modules: `node:module` API | Node.js v26.3.1 Documentation</a></li>

</ul>
</details>

**社区讨论**: 社区反应热烈，有用户报告说他们的整个 monorepo 无缝迁移到了 Nub。一些用户质疑在 Node 原生支持 TypeScript 的情况下是否需要转译器，而另一些用户则讨论了 ESM 支持的细微差别以及选择 --require 而非 --import 的原因。

**标签**: `#Node.js`, `#tooling`, `#developer experience`, `#TypeScript`, `#Bun`

---

<a id="item-4"></a>
## [间谍软件利用违禁文本逃避 AI 分析](https://www.schneier.com/blog/archives/2026/06/embedding-forbidden-text-in-spyware-to-discourage-ai-analysis-2.html) ⭐️ 8.0/10

恶意软件开发者正在间谍软件的 JavaScript 注释块中嵌入核武器和生物武器相关文本，以触发 AI 分析工具的内容政策拒绝，导致工具跳过或错误分类恶意代码。 这种新颖的对抗性技术削弱了 AI 驱动恶意软件检测的可靠性，可能迫使安全供应商重新设计分析管道以应对此类规避策略，凸显了攻击者与 AI 防御之间日益升级的军备竞赛。 违禁文本被放置在一个大型 JavaScript 块注释中，不影响执行，但会被 AI 扫描器读取，可能因违反政策而拒绝分析文件。真正的恶意代码随后以 try{eval(...)}包装器和 ROT 风格替换函数的形式出现。

rss · Schneier on Security · 6月24日 11:03

**背景**: 基于 AI 的恶意软件分析工具通常使用大型语言模型检查代码片段，而许多 LLM 经过训练，具有拒绝生成或处理大规模杀伤性武器相关内容的安全策略。通过嵌入此类违禁文本，攻击者可以触发这些拒绝机制，导致 AI 在分析到实际恶意负载之前中止分析。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cambridgeanalytica.org/ai-machine-learning/hackers-hiding-spyware-forbidden-text-ai-scanners-51128/">Hackers Just Started Hiding Spyware Inside Forbidden Text to</a></li>

</ul>
</details>

**社区讨论**: 在 X（原 Twitter）和 Socket.dev 上的社区讨论指出，这种技术已在野外被观察到，研究人员认为它利用了当前 AI 分析管道的一个根本弱点。一些评论者认为这种方法很巧妙，但随着防御者通过剥离注释或使用独立扫描器来适应，它可能很快失效。

**标签**: `#malware`, `#AI safety`, `#adversarial attacks`, `#cybersecurity`, `#spyware`

---

<a id="item-5"></a>
## [zrip：纯 Rust 实现的 Zstd 编解码器，优化传输速度](https://www.reddit.com/r/rust/comments/1uebc33/zrip_a_fromscratch_zstd_codec_in_pure_rust/) ⭐️ 8.0/10

一个名为 zrip 的全新 Zstd 编解码器以纯 Rust 发布，专注于快速数据传输而非归档存储。它支持压缩级别 -7 到 4，采用 Fast 和 DFast 策略，并内置了 COVER 和 FastCOVER 字典训练功能。 zrip 是目前最快的纯 Rust Zstd 实现，性能优于 ruzstd 和 structured-zstd 等替代方案，在 WASM 环境中甚至超过了编译为 WASM 的 C zstd。这使其成为 Rust 生态系统中高速数据传输管道的强有力候选，尤其适用于小消息工作负载。 代码库约 12000 行 Rust 代码，unsafe 代码仅限于小型基础模块，并通过 debug_assert! 检查保护。'paranoid' 特性使用纯安全 Rust 且无 SIMD，但速度仍比 ruzstd 快两倍。

reddit · r/rust · /u/event666 · 6月24日 11:51

**背景**: Zstd（Zstandard）是 Facebook 开发的一种快速压缩算法，广泛用于数据传输和存储中的实时压缩。纯 Rust 实现因其安全性和可移植性而备受青睐，但历史上性能一直落后于 C 参考实现。zrip 旨在缩小这一差距，专注于传输场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/yoshihitoh/zstd-codec">GitHub - yoshihitoh/ zstd - codec : Zstandard codec for Node.js and Web...</a></li>
<li><a href="https://deepwiki.com/facebook/zstd/5.1-dictionary-training-algorithms">Dictionary Training Algorithms | facebook/zstd | DeepWiki</a></li>
<li><a href="https://deepwiki.com/facebook/zstd/5-dictionary-system">Dictionary System | facebook/zstd | DeepWiki</a></li>

</ul>
</details>

**社区讨论**: Reddit 讨论突显了该项目的技术深度，用户称赞其详细的基准测试和设计权衡。一些评论者指出，专注于传输速度而非压缩比是一个明智的细分方向，而另一些人则对更高压缩级别的潜在改进表示兴趣。

**标签**: `#rust`, `#compression`, `#zstd`, `#performance`, `#open-source`

---

<a id="item-6"></a>
## [Bunny DNS 免费：无查询费，支持 500 个域名](https://bunny.net/blog/were-making-bunny-dns-free/) ⭐️ 7.0/10

Bunny.net 宣布 Bunny DNS 现已免费，取消了所有 DNS 查询费用，并为每个账户提供最多 500 个域名的免费 DNS 托管。 此举使 Bunny DNS 成为 Cloudflare DNS 服务的强大欧盟替代方案，可能吸引那些关注欧美数据地缘政治并寻求有竞争力的欧洲技术选项的用户。 免费层包括无查询限制、无按请求计费，并可访问智能记录和健康监控等功能，这些功能在其他服务商通常被隐藏在企业计划之后。

hackernews · dabinat · 6月24日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48657030)

**背景**: DNS（域名系统）将域名转换为 IP 地址。许多 DNS 提供商按查询量收费或提供有限的免费层。Bunny.net 是一家私营公司，仅在 2022 年进行了一轮 600 万美元的融资，专注于有机增长而非投资者资助的扩张。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bunny.net/dns/">Bunny DNS | The #1 Scriptable DNS Platform | bunny.net</a></li>
<li><a href="https://bunny.net/blog/2022-in-review-reflecting-on-last-years-highlights/">2022 in Review: Bunny.net's Year of Milestones and</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎这一举措，一些人称赞 Bunny 是欧盟的 Cloudflare 替代品，另一些人则注意到该公司可持续的商业模式。然而，也有人担心机器人流量带来的意外费用，以及非 CDN 产品缺乏账单上限。

**标签**: `#DNS`, `#cloud`, `#EU tech`, `#free service`, `#Bunny.net`

---

<a id="item-7"></a>
## [RubyLLM：面向主要 AI 提供商的统一 Ruby 框架](https://rubyllm.com/) ⭐️ 7.0/10

RubyLLM 是一个 Ruby 框架，为多个主要 AI 提供商（包括 OpenAI、Anthropic、Google 等）提供统一接口。它通过将 API 调用、流式传输和图像生成标准化为一致的 Ruby API 来简化集成。 该框架填补了 Ruby 生态系统中 AI 集成的空白，使 Ruby 开发者能够更轻松地构建基于 LLM 的应用，而无需在不同提供商的 SDK 之间切换。它在 Hacker News 上获得 339 分，表明社区兴趣浓厚且实际需求旺盛。 RubyLLM 维护已知模型和提供商的注册表，但允许显式指定提供商或使用自定义端点。它将流式传输格式标准化为统一的 Chunk 对象，并支持可配置默认模型的图像生成。

hackernews · doener · 6月24日 14:41 · [社区讨论](https://news.ycombinator.com/item?id=48660711)

**背景**: Ruby 开发者长期以来缺乏针对 LLM API 的统一抽象层，通常需要为每个提供商使用单独的 SDK。RubyLLM 旨在提供类似 Rails 的开发体验，类似于 Vercel 的 AI SDK 对 JavaScript 的作用。该框架是开源的，并催生了 Raix 等社区扩展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rubyllm.com/overview/">Overview | RubyLLM</a></li>
<li><a href="https://rubyllm.com/image-generation/">Image Generation | RubyLLM</a></li>
<li><a href="https://rubyllm.com/streaming/">Stream Responses | RubyLLM</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞 RubyLLM 易用且 API 简洁，但也指出了实际痛点：与 xAI 等提供商的缓存问题、对 responses API 缺乏原生支持（尽管最近已添加），以及难以实现真正的链路可观测性。部分用户质疑在单一提供商项目中，使用该框架相比直接使用 SDK 的优势。

**标签**: `#Ruby`, `#AI framework`, `#LLM`, `#developer tools`, `#API integration`

---

<a id="item-8"></a>
## [GitHub 上的 PR 垃圾信息与早期邮件垃圾信息如出一辙](https://www.greptile.com/blog/prs-on-openclaw) ⭐️ 7.0/10

一篇博客文章和社区讨论将当前 GitHub 上的 PR 垃圾信息与 21 世纪初的邮件垃圾信息相提并论，强调了需要更好的维护者工具和社区规范。 这种比较凸显了开源维护者面临的一个日益严重的问题：低质量或自动化的拉取请求数量不断增加，威胁到项目健康和贡献者信任。 像 Spampr 和 Fossier 这样的工具已经出现，可以自动标记或拒绝来自非可信贡献者的 PR，而 GitHub 最近也为维护者添加了可配置的 PR 限制。

hackernews · dakshgupta · 6月24日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=48660579)

**背景**: 21 世纪初的邮件垃圾信息是一种普遍的滋扰，导致了过滤技术和发件人信誉系统的发展。类似地，GitHub 上的 PR 垃圾信息涉及自动化或低质量的拉取请求，浪费维护者的时间并降低项目质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/marketplace/spampr">Spampr - GitHub Marketplace</a></li>
<li><a href="https://github.com/PThorpe92/fossier">GitHub - PThorpe92/fossier: Vouch-compatible PR-spam ...</a></li>
<li><a href="https://github.blog/open-source/maintainers/new-tools-for-open-source-maintainers/">New tools for open source maintainers - The GitHub Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者指出了关键差异，例如邮件垃圾信息依赖于服务器信誉，而 PR 垃圾信息针对个人用户。建议包括要求新贡献者在合并前与维护者会面，以及允许捐赠代币积分供维护者使用。

**标签**: `#open source`, `#spam`, `#GitHub`, `#maintainer tools`, `#community`

---

<a id="item-9"></a>
## [NVIDIA 45°C 冷却方案大幅降低数据中心用水](https://blogs.nvidia.com/blog/liquid-cooling-ai-factories/) ⭐️ 7.0/10

NVIDIA 为其 Rubin 代 AI 工厂推出了 45°C 液冷架构，通过使用更高温度的冷却液并直接将热量排放到环境空气中，在有利气候下几乎可以消除水消耗。 该设计解决了 AI 数据中心日益突出的用水环境问题，每个设施可节省数百万加仑水，并支持更可持续的 AI 基础设施扩展。 冷却液是 75% 水和 25% 丙二醇的混合物，以 45°C 进入处理器，约 55°C 排出。冷却装置温度每升高 1°C，冷却能耗成本约降低 4%，而冷却可占数据中心总用电量的 40%。

hackernews · nitin_flanker · 6月24日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48660178)

**背景**: 传统数据中心使用空调或带冷却装置的液冷系统，消耗大量水和能源。液冷通常使用较低温度（约 20-30°C）并需要高能耗冷却装置。NVIDIA 的方法使用更热的冷却液回路，在许多气候下可通过环境空气冷却，从而减少或消除对蒸发冷却和用水的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://beyondtmrw.org/article/45c-breakthrough-to-cool-ai-data-center-machines">AI Data Center Liquid Cooling 45C: Hotter Than a Hot Tub</a></li>
<li><a href="https://www.guru3d.com/story/nvidia-unveils-liquid-cooling-design-for-ai-data-centers/">NVIDIA Unveils 45°C Liquid Cooling Design for AI Data Centers</a></li>
<li><a href="https://icharles.com/articles/nvidia-rubin-45c-liquid-cooling-zero-water">NVIDIA Rubin: 45°C Cooling, Near-Zero Water · iCharles</a></li>

</ul>
</details>

**社区讨论**: 评论者质疑“零用水”的定义以及 45°C 冷却在不同气候下的实用性。一些人注意到与区域供热的潜在协同效应，而另一些人则批评完全消除用水的说法，认为水仍在循环且必须来自某处。

**标签**: `#data centers`, `#cooling`, `#AI infrastructure`, `#sustainability`, `#NVIDIA`

---

<a id="item-10"></a>
## [Elastic 裁员 7%，归因于 AI](https://www.elastic.co/blog/ceo-ash-kulkarni-announcement-to-elastic-employees) ⭐️ 7.0/10

Elasticsearch 背后的公司 Elastic 宣布裁员 7%，并将重组归因于 AI 和自动化的进步。 此次裁员反映了科技公司以 AI 为理由裁减员工，同时计划招聘市场推广岗位的趋势，引发了关于企业优先级的讨论。 公司计划在销售和营销等市场推广岗位增加招聘，作为简化运营和聚焦增长的重组的一部分。

hackernews · dakrone · 6月24日 21:57 · [社区讨论](https://news.ycombinator.com/item?id=48666100)

**背景**: Elastic 以其开源搜索和分析引擎 Elasticsearch 闻名，广泛用于日志分析和企业搜索。科技行业裁员已变得普遍，但明确将裁员与 AI 联系起来是一种较新的现象，批评者认为这可能是削减成本的借口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.elastic.co/about/">Hi, we're Elastic | Elastic</a></li>
<li><a href="https://prospeo.io/s/go-to-market-roles">Go - to - Market Roles Explained: Modern GTM Team Map (2026)</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了怀疑，一些人指出在 1980 年代之前裁员很少见，且公告更多地关注未来乐观前景而非受影响的员工。前员工表示悲伤，一个翻译网站讽刺地重新解读了企业语言。

**标签**: `#layoffs`, `#tech industry`, `#AI`, `#Elastic`, `#corporate culture`

---

<a id="item-11"></a>
## [Xteink X4：基于微控制器的极简开源电子墨水阅读器](https://blog.omgmog.net/post/xteink-x4-e-ink-reader/) ⭐️ 7.0/10

Xteink X4 是一款信用卡大小的电子墨水阅读器，基于 ESP32 微控制器并支持 WiFi，提供极简、开源的阅读体验。它因其可破解性和简洁性受到社区关注，但缺少背光且屏幕较小。 X4 证明了微控制器足以实现功能完整的电子阅读器，挑战了 Kindle 等封闭设备的统治地位。其开放性鼓励定制，可能激发更廉价、可破解的电子阅读器。 X4 配备 2.7 英寸电子墨水屏、USB-C 充电和磁性保护套，便于携带。它可运行 CrossPoint 或 Papyrix 等自定义固件，其支持 WiFi 的 HTTP 服务器简化了书籍传输。

hackernews · felixdoerp · 6月24日 16:35 · [社区讨论](https://news.ycombinator.com/item?id=48662381)

**背景**: Kindle 等电子墨水阅读器使用低功耗屏幕，断电后仍能保留文字，适合长时间阅读。大多数商用电子阅读器运行基于 Linux 的系统，软件专有，限制了用户修改。基于微控制器的阅读器（如使用 ESP32 或 RP2040 的）成本更低，可完全控制硬件和软件，但通常屏幕较小、功能较少。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ereadersforum.com/threads/xteink-x4-e-ink-reader-review-a-compact-concept-with-significant-limitations.12676/">Xteink X4 E-Ink Reader Review: A Compact Concept With</a></li>
<li><a href="https://www.androidpolice.com/trick-turned-e-reader-into-a-must-buy/">This simple trick transformed my disappointing Xteink X4</a></li>
<li><a href="https://solariz.de/posts/26/04-xteink-x4-ereader-papyrix-firmware/">New gadget; Xteink X4 E-Ink reader flashed with Papyrix |</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞 X4 的简洁性和可破解性，有人将其用作便携的辅助阅读器。但许多人指出屏幕小且无背光是致命缺陷，尤其对年长用户。建议包括更大屏幕、更高 DPI 和更好的休眠功耗。

**标签**: `#e-ink`, `#e-reader`, `#hardware`, `#open-source`, `#microcontroller`

---

<a id="item-12"></a>
## [卡马克反思 id Software 早期管理失误](https://twitter.com/ID_AA_Carmack/status/2069799283369345247) ⭐️ 7.0/10

约翰·卡马克在 Twitter 上发文，反思自己在 id Software 早期犯下的错误，包括对员工要求过于严苛，以及未能随着公司成熟而调整管理风格。 这位传奇游戏开发者的回顾为创业文化和管理提供了宝贵经验，凸显了技术雄心与可持续团队动态之间的张力。 卡马克特别指出，持续以创业强度要求员工会让他们精疲力竭，而成熟的公司需要更多的宽松空间。该帖子在 Hacker News 上获得了 485 分和 241 条评论。

hackernews · shadowtree · 6月24日 15:56 · [社区讨论](https://news.ycombinator.com/item?id=48661825)

**背景**: 约翰·卡马克是 id Software 的联合创始人，以在《德军总部 3D》、《毁灭战士》和《雷神之锤》等游戏中开创 3D 图形技术而闻名。id Software 从一个小型创业公司迅速成长为大型工作室，卡马克的技术才华是其成功的关键，但他的管理风格据称导致了员工倦怠。

**社区讨论**: 评论者普遍认同卡马克的自我批评，有人指出桑迪·彼得森等具体离职事件作为证据。其他人则注意到，尽管内部压力巨大，但产出的游戏具有开创性，值得付出代价。

**标签**: `#game development`, `#management`, `#startup culture`, `#id Software`, `#John Carmack`

---

<a id="item-13"></a>
## [Rust 社区推动 crates.io 与 GitHub 解耦](https://infosec.exchange/@mttaggart/116806641273303255) ⭐️ 7.0/10

Rust 社区正在积极讨论并致力于将 crates.io 的发布与 GitHub 解耦，相关 RFC 已合并，实现工作正在进行中。 这一变化将降低供应链风险和供应商锁定，使 Rust 生态系统更具弹性，并独立于单一平台。 这项工作由志愿者驱动，由于工作复杂且资金有限而面临挑战；存在包含具体任务的路由图，欢迎贡献。

hackernews · speckx · 6月24日 19:40 · [社区讨论](https://news.ycombinator.com/item?id=48664733)

**背景**: 目前，向 crates.io 发布 crate 需要通过 GitHub 账户进行身份验证，从而产生了对 GitHub 的依赖。Rust 项目早已认识到这是一个问题，但由于项目的志愿者性质，进展缓慢。

**社区讨论**: 社区评论承认问题存在且工作正在进行，但指出进展缓慢，因为这是一项庞大且无趣的任务，志愿者没有报酬。有人建议参考其他注册中心如 Packagist 的做法。

**标签**: `#Rust`, `#crates.io`, `#supply chain`, `#open source`, `#GitHub`

---

<a id="item-14"></a>
## [LWN 周刊：自由线程 Python、AUR 攻击、BPF arena](https://lwn.net/Articles/1078380/) ⭐️ 7.0/10

2026 年 6 月 25 日的 LWN.net 周刊涵盖了自由线程 Python、对 Arch 用户仓库（AUR）的攻击、Fedora 的双因素认证计划，以及包括 arena 和协程在内的新 BPF 特性。 这些话题反映了 Linux 和开源生态系统的关键发展，从 Python 的性能改进到软件仓库的安全挑战，再到内核级编程的进步。 本期还讨论了 7.2 合并窗口、BPF JIT 改进和 OSPM（操作系统电源管理）。BPF arena 允许在验证器中安全地放宽指针检查，从而支持复杂数据结构。

rss · LWN.net · 6月25日 00:54

**背景**: LWN.net 是备受尊敬的 Linux 内核和开源新闻来源。BPF（伯克利包过滤器）是一种用于运行沙盒程序的内核技术；arena 和协程是其最新的扩展，旨在提升其能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lwn.net/Articles/1019885/">A look at what's possible with BPF arenas [LWN.net]</a></li>
<li><a href="https://lwn.net/Articles/961128/">bpf: Introduce BPF arena. [LWN.net]</a></li>
<li><a href="https://bpfconf.ebpf.io/bpfconf2026/bpfconf2026_material/Coroutines+in+BPF+-+LSF_MM_BPF+May+2026.pdf">PDF Coroutines in BPF - LSF/MM/BPF May 2026 - bpfconf.ebpf.io</a></li>

</ul>
</details>

**标签**: `#Linux`, `#kernel`, `#open-source`, `#Python`, `#BPF`

---

<a id="item-15"></a>
## [Fedora 将在安全事件后要求 Provenpackager 启用双因素认证](https://lwn.net/Articles/1078964/) ⭐️ 7.0/10

Fedora 计划在未来三个月内要求所有 provenpackager 启用双因素认证（2FA），此前发生了一起疑似账户被入侵事件，导致一个 AI 代理给项目造成了问题。 这一政策变更解决了开源供应链中的一个关键安全漏洞，因为账户被入侵是恶意软件注入的常见途径。它为其他发行版和项目加强认证要求树立了先例。 该要求最初仅适用于 provenpackager 群体，该群体拥有修改仓库中任何软件包的提升权限。合规期限约为三个月。

rss · LWN.net · 6月24日 17:01

**背景**: 双因素认证（2FA）在密码之外增加了第二个验证步骤，降低了账户被接管的风险。Provenpackager 是受信任的 Fedora 贡献者，可以修改任何软件包，因此成为攻击者的高价值目标。该事件涉及一个 AI 代理，在 provenpackager 账户疑似被入侵后造成了混乱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.fedoraproject.org/en-US/fesco/Provenpackager_policy/">Policy for provenpackagers :: Fedora Docs</a></li>

</ul>
</details>

**标签**: `#security`, `#open-source`, `#supply chain`, `#Fedora`, `#authentication`

---

