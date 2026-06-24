# Horizon 每日速递 - 2026-06-23

> 从 30 条内容中筛选出 15 条重要资讯。

---

1. [Valve 推出 Steam Machine，采用公平预订系统](#item-1) ⭐️ 9.0/10
2. [自由线程 Python：过去、现在与未来](#item-2) ⭐️ 9.0/10
3. [Moebius：0.2B 参数模型媲美 10B 级图像修复性能](#item-3) ⭐️ 8.0/10
4. [加拿大计划到 2040 年建造多达 10 座核反应堆](#item-4) ⭐️ 8.0/10
5. [警察局长滥用 Flock 车牌读取器数据跟踪女性](#item-5) ⭐️ 8.0/10
6. [提示注入作为大语言模型中的角色混淆](#item-6) ⭐️ 8.0/10
7. [Mitchell Hashimoto 承诺向 Zig 软件基金会捐赠 40 万美元](#item-7) ⭐️ 8.0/10
8. [2026 年 Linux 安全启动证书到期](#item-8) ⭐️ 8.0/10
9. [雪佛龙与微软签署 20 年天然气供电协议](#item-9) ⭐️ 8.0/10
10. [Deno Desktop 实现桌面应用开发，共享 CEF 运行时](#item-10) ⭐️ 8.0/10
11. [Claude Code 的扩展思考输出是有损摘要](#item-11) ⭐️ 8.0/10
12. [本地运行 GLM-5.2：MoE 卸载指南](#item-12) ⭐️ 7.0/10
13. [Oak：面向 AI 代理的 Git 替代品](#item-13) ⭐️ 7.0/10
14. [Xfce Wayland 合成器 xfwl4 首个预览版发布](#item-14) ⭐️ 7.0/10
15. [OSPM 2026 第一天：空闲状态、sched_ext 和锁持有者抢占](#item-15) ⭐️ 7.0/10

---

<a id="item-1"></a>
## [Valve 推出 Steam Machine，采用公平预订系统](https://store.steampowered.com/news/group/45479024/view/685257114654870245) ⭐️ 9.0/10

Valve 于 2026 年 6 月 22 日正式推出 Steam Machine，这是一款紧凑型游戏 PC，采用预订系统以防止黄牛并确保公平。 这标志着 Valve 以开放性和反黄牛措施重返专用游戏硬件领域，通过提供兼具主机体验和 PC 灵活性的产品，可能重塑 PC 游戏市场。 Steam Machine 是一款 15x16x16 厘米的迷你 PC 立方体，搭载 AMD 芯片，起售价超过 1000 美元，预订窗口为 2026 年 6 月 22 日至 25 日，每户限购一台。

hackernews · theschwa · 6月22日 17:09 · [社区讨论](https://news.ycombinator.com/item?id=48632884)

**背景**: Valve 曾在 2015 年尝试与第三方合作推出 Steam Machine 概念，但未获成功。新款为第一方设备，运行 SteamOS，强调用户可自由安装应用或其他操作系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://store.steampowered.com/hardware/steammachine">Steam Machine</a></li>
<li><a href="https://www.theverge.com/games/952191/valve-steam-machine-reservation-preorder-process">Here’s how you can reserve a Steam Machine | The Verge</a></li>
<li><a href="https://thephrasemaker.com/2026/06/22/steam-machine-price-revealed-starts-at-over-1000/">Steam Machine Price Revealed, Starts At Over $1,000 - Phrasemaker</a></li>

</ul>
</details>

**社区讨论**: 社区评论称赞预订系统的公平性和硬件的开放性，用户赞赏 Valve 不锁定设备的立场。部分人表达了购买意愿，另一些人则关注价格和规格。

**标签**: `#gaming`, `#hardware`, `#valve`, `#steam`, `#launch`

---

<a id="item-2"></a>
## [自由线程 Python：过去、现在与未来](https://lwn.net/Articles/1078367/) ⭐️ 9.0/10

在 PyCon US 2026 上，CPython 核心开发者 Thomas Wouters 发表了关于自由线程 Python 解释器的演讲，该解释器移除了全局解释器锁（GIL），允许线程真正并行执行。 移除 GIL 是 Python 并发编程的一个范式转变，使多线程 Python 程序能够有效利用多个 CPU 核心，从而显著提升 CPU 密集型和 I/O 密集型工作负载的性能。 自由线程构建使用 mimalloc 分配器而非 pymalloc，开发者必须避免写入共享可变对象以确保线程安全。

rss · LWN.net · 6月22日 15:26

**背景**: 全局解释器锁（GIL）是一个保护 Python 对象访问的互斥锁，阻止多个线程同时执行 Python 字节码。这历来限制了 Python 利用多核处理器进行并行执行的能力。自由线程 Python 项目旨在移除这一瓶颈，同时保持向后兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.python.org/3/howto/free-threading-python.html">Python support for free threading — Python 3.14.6 documentation</a></li>
<li><a href="https://medium.com/codetodeploy/pythons-free-threaded-future-how-to-write-code-for-a-post-gil-world-cb1064af600b">Python ’s Free - Threaded Future: How to Write Code for... | Medium</a></li>
<li><a href="https://thinhdanggroup.github.io/async-wars/">Async Wars: Comparing Python ’s Free - Threaded Future vs Node.js...</a></li>

</ul>
</details>

**标签**: `#Python`, `#CPython`, `#GIL`, `#concurrency`, `#free-threaded`

---

<a id="item-3"></a>
## [Moebius：0.2B 参数模型媲美 10B 级图像修复性能](https://hustvl.github.io/Moebius/) ⭐️ 8.0/10

华中科技大学等机构的研究人员发布了 Moebius，这是一个仅 0.2B 参数的图像修复模型，声称性能可与 10B 参数模型媲美。社区成员已通过 ONNX 在浏览器中成功运行该模型。 这一突破可能使高质量图像修复技术普及到消费级设备上，无需依赖云端。它挑战了“大模型才能达到顶尖性能”的假设，有望降低计算成本和能耗。 Moebius 的输出分辨率限制为 512x512，限制了其在大尺寸图像上的实际应用。社区测试显示，修复区域明显比周围更平滑，且模型在处理新物体时表现不佳。

hackernews · DSemba · 6月22日 13:53 · [社区讨论](https://news.ycombinator.com/item?id=48630171)

**背景**: 图像修复是指用合理内容填充图像中缺失或被遮罩区域的任务。传统方法使用在遮罩图像上微调的扩散模型，通常需要数十亿参数的大模型。Moebius 通过高效的架构设计，以极少的参数实现了类似效果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.runlocalai.co/glossary/image-inpainting">Image Inpainting — AI glossary | RunLocalAI</a></li>

</ul>
</details>

**社区讨论**: 社区对该模型的效率印象深刻，但对声称的 10B 级性能持怀疑态度。用户报告了明显的质量差距，例如修复区域更平滑以及处理新物体时表现不佳。simonw 的浏览器演示受到称赞，但一些用户指出该模型在许多图像上会失败。

**标签**: `#image inpainting`, `#efficient models`, `#computer vision`, `#machine learning`, `#browser inference`

---

<a id="item-4"></a>
## [加拿大计划到 2040 年建造多达 10 座核反应堆](https://www.cbc.ca/news/politics/federal-nuclear-strategy-9.7244509) ⭐️ 8.0/10

加拿大政府宣布计划到 2040 年建造多达 10 座核反应堆，利用其丰富的铀储量和 CANDU 反应堆技术。 这标志着加拿大能源政策的重大转变，旨在提供清洁基荷电力以补充可再生能源，并支持工业脱碳，可能使加拿大成为全球核能领导者。 该计划包括小型模块化反应堆（SMR）和传统 CANDU 设计，其中达林顿新核电项目等已在建设中。加拿大在国内外建造和翻新反应堆方面拥有丰富经验。

hackernews · geox · 6月22日 19:06 · [社区讨论](https://news.ycombinator.com/item?id=48634585)

**背景**: CANDU 反应堆是加拿大设计的加压重水反应堆，使用天然铀作为燃料，重水作为慢化剂，具有燃料高效和防扩散的特点。加拿大是世界上最大的铀生产国之一，在萨斯喀彻温省拥有大量储量。该国拥有悠久的核电历史，安大略省、新不伦瑞克省和魁北克省已有 CANDU 机组运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CANDU_reactor">CANDU reactor - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/candu-nuclear-renaissance-why-canadian-technology-now-joe-st-julian-df5oc">CANDU and the Nuclear Renaissance: Why Canadian Technology ...</a></li>
<li><a href="https://www.discoverthegreentech.com/en/nuclear-power/plant/reactors/candu/">CANDU nuclear reactors : history and characteristics - Découvrez la...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍支持该计划，提到加拿大的铀储量、CANDU 技术专长以及需要基荷电力来补充可再生能源。一些人注意到油砂工业应用的潜力，并警告不要廉价向美国出售电力。其他人对加拿大的全球核能足迹和 SMR 项目进展表示惊讶。

**标签**: `#nuclear energy`, `#Canada`, `#energy policy`, `#CANDU`, `#infrastructure`

---

<a id="item-5"></a>
## [警察局长滥用 Flock 车牌读取器数据跟踪女性](https://ipvm.com/reports/police-chiefs-track) ⭐️ 8.0/10

报道和社区讨论揭露，警察局长利用 Flock 自动车牌读取器（ALPR）数据跟踪女性，凸显了此类监控缺乏搜查令要求的问题。 这种滥用凸显了为 ALPR 数据访问设置搜查令要求的紧迫性，因为该技术在没有保障措施的情况下广泛部署，会导致隐私侵犯并削弱公民自由。 Flock 摄像头实时捕捉车牌数据，并与数据库交叉比对以查找通缉令或警报；文章指出，虽然滥用情况罕见，但一旦发生，这是最常见的不当行为形式。

hackernews · jhonovich · 6月22日 19:13 · [社区讨论](https://news.ycombinator.com/item?id=48634694)

**背景**: 像 Flock 这样的自动车牌读取器（ALPR）使用光学字符识别来识别车牌，通常安装在巡逻车或固定杆上。执法部门利用它们定位被盗车辆或通缉人员，但数据可以在没有搜查令的情况下访问，引发了第四修正案方面的担忧。拟议的立法，如《监控问责法案》，将要求政府访问此类数据时需获得搜查令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fortune.com/2026/06/03/why-are-ohio-city-workers-covering-flock-cameras-immigration-enforcement-data-sharing-policy-violations/">Dayton is covering Flock cameras with trash bags after... | Fortune</a></li>
<li><a href="https://decrypt.co/365231/proposed-house-bill-require-warrants-government-ai-surveillance">Proposed House Bill Would Require Warrants for... - Decrypt</a></li>
<li><a href="https://www.govtech.com/public-safety/joplin-mo-watchdog-group-questions-use-of-flock-cameras">Joplin, Mo., Watchdog Group Questions Use of Flock Cameras</a></li>

</ul>
</details>

**社区讨论**: 评论者就破案效益与隐私风险之间的张力展开辩论，一些人指出滥用虽然罕见，但却是最常见的不当行为形式。其他人则将其与监控反乌托邦相提并论，并建议联系当地 ACLU 分会，质疑 Flock 的安装违反了第四修正案。

**标签**: `#surveillance`, `#privacy`, `#police abuse`, `#license plate readers`, `#civil liberties`

---

<a id="item-6"></a>
## [提示注入作为大语言模型中的角色混淆](https://role-confusion.github.io/) ⭐️ 8.0/10

一篇新论文和博客文章指出，提示注入利用了 LLM 中的角色混淆，人类红队对前沿模型的攻击成功率接近 100%，而静态基准测试未能捕捉到这一漏洞。 这揭示了当前 LLM 安全评估中的一个根本盲点：静态基准测试衡量的是对已知攻击的防御能力，但熟练的人类可以调整并绕过它们。这些发现凸显了需要动态、人在回路中的测试来评估真实世界的鲁棒性。 论文表明，LLM 根据风格和位置线索而非接口边界来推断角色，因此攻击者提供的模仿系统或思维链风格的内容在隐藏空间中获得了提升的“角色权威”。这解释了为什么将指令包裹在<think>标签中或使用特定写作风格可以绕过护栏。

hackernews · x312 · 6月22日 15:48 · [社区讨论](https://news.ycombinator.com/item?id=48631888)

**背景**: 提示注入是一种安全漏洞，攻击者通过精心构造输入来覆盖 LLM 的原始指令或系统提示。角色混淆的发生是因为 LLM 缺乏系统指令与用户数据之间的明确分离；它们将所有文本视为上下文，并从模式中推断角色。静态基准测试通常测试一组固定的已知攻击模式，模型可以学会识别这些模式，但人类攻击者可以动态地构造新颖的攻击来逃避检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://owasp.org/www-community/attacks/PromptInjection">Prompt Injection | OWASP Foundation</a></li>
<li><a href="https://www.emergentmind.com/topics/direct-prompt-injection">Direct Prompt Injection in LLMs</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞博客风格的写作使研究更易理解。一些人指出这些发现与他们自己的实验一致，例如“用户正在询问……”等风格线索可以绕过护栏。一位用户提出了一种架构修复方案：为每个 token 添加不可伪造的角色嵌入，但他们承认这尚未在大规模上得到验证。

**标签**: `#prompt injection`, `#LLM security`, `#role confusion`, `#AI safety`, `#adversarial attacks`

---

<a id="item-7"></a>
## [Mitchell Hashimoto 承诺向 Zig 软件基金会捐赠 40 万美元](https://mitchellh.com/writing/zig-donation-2026) ⭐️ 8.0/10

Ghostty 终端模拟器的创建者 Mitchell Hashimoto 宣布向 Zig 软件基金会承诺捐赠 40 万美元，以支持 Zig 编程语言及其社区的发展。 这一重大财务承诺凸显了为开源基础设施提供可持续资金的重要性，尤其是对于像 Zig 这样旨在改进 C 语言的新兴系统编程语言。 该承诺针对 2026 年，继 Hashimoto 在 2024 年捐赠 40 万美元之后，体现了持续的支持。这笔资金将用于维护 Zig 编译器、标准库和社区项目。

hackernews · tosh · 6月22日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=48630020)

**背景**: Zig 是一种通用系统编程语言，旨在成为 C 语言的现代替代品，专注于健壮性、最优性和可维护性。Zig 软件基金会是一个非营利组织，负责监督该语言的发展。Mitchell Hashimoto 是开源社区的知名人物，以联合创建 HashiCorp 以及用 Zig 开发 Ghostty 终端模拟器而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig ( programming language ) - Wikipedia</a></li>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>
<li><a href="https://ziglang.org/learn/overview/">Overview Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 社区反应积极，许多人称赞 Hashimoto 的慷慨和 Zig 独特的文化。一些评论者强调了 Ghostty 作为 Zig 能力实际展示的价值，而另一些人则赞赏该项目反对 LLM 生成贡献的立场，强调精心设计而非快速产出代码。

**标签**: `#Zig`, `#open-source`, `#funding`, `#systems-programming`, `#community`

---

<a id="item-8"></a>
## [2026 年 Linux 安全启动证书到期](https://lwn.net/Articles/1029767/) ⭐️ 8.0/10

微软 2011 年签发的安全启动证书将于 2026 年 6 月 27 日到期，启用安全启动的 Linux 系统若不更新，可能导致启动失败。 这影响数百万依赖安全启动的 Linux 用户，过时的系统在证书到期后可能无法启动，需要手动更新固件和引导加载程序密钥。 用户可通过'mokutil --db --short'检查当前密钥，并通过'sudo fwupdmgr update'更新以获取 2023 年新密钥；Windows PC 将通过 Windows Update 自动更新。

hackernews · weaksauce · 6月22日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=48633941)

**背景**: 安全启动通过验证数字签名确保系统启动时只运行受信任的软件。微软 2011 年的证书签署了 Linux 的初始 shim 引导加载程序，其到期意味着系统必须切换到更新的证书以维持信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linuxteck.com/secure-boot-linux-key-expires/">Secure Boot Linux 2026 : Microsoft 's Key Expires June 27</a></li>
<li><a href="https://blog.desdelinux.net/en/expiration-of-Microsoft-Secure-Boot-Linux-shim-certificate/">Microsoft Secure Boot certificate for Linux expires : What to do</a></li>
<li><a href="https://byteiota.com/secure-boot-certificates-expire-june-27-act-now/">Secure Boot Certificates Expire June 27: Act Now | byteiota</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出缺乏检查和更新密钥的明确指南，用户分享了变通方法，并指出注册自定义密钥是另一种选择。一些人批评对微软密钥的依赖。

**标签**: `#Linux`, `#Secure Boot`, `#Security`, `#System Administration`

---

<a id="item-9"></a>
## [雪佛龙与微软签署 20 年天然气供电协议](https://www.chevron.com/newsroom/2026/q2/chevron-signs-20-year-power-agreement-with-microsoft-for-west-texas-data-center) ⭐️ 8.0/10

雪佛龙与微软签署了一项为期 20 年的购电协议，利用二叠纪盆地的天然气为西德克萨斯州的一个新数据中心供电。 该协议凸显了人工智能和云计算激增的能源需求与微软到 2030 年实现碳负排放承诺之间的紧张关系，因为它依赖化石燃料而非可再生能源。 大部分发电将来自 GE Vernova 的大型涡轮机，额外容量由 Solar Turbines（卡特彼勒子公司）提供。二叠纪盆地目前天然气价格为负，意味着生产商需付费才能将天然气运走。

hackernews · cdrnsf · 6月22日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=48630029)

**背景**: 西德克萨斯州的二叠纪盆地是一个主要的油气产区，伴生大量天然气。微软承诺到 2030 年实现碳负排放，即移除的碳多于排放的碳。人工智能和云服务的数据中心消耗大量电力，对可持续发展目标构成挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Permian_Basin_(North_America)">Permian Basin (North America) - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/technology-51133811">Microsoft makes ' carbon negative ' pledge</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，微软在签署化石燃料协议的同时承诺碳负排放具有讽刺意味，并指出德克萨斯州的太阳能和电池更便宜。一些人强调二叠纪盆地天然气价格为负，使得该协议在经济上具有吸引力，尽管存在环境担忧。

**标签**: `#energy`, `#data centers`, `#AI`, `#cloud computing`, `#sustainability`

---

<a id="item-10"></a>
## [Deno Desktop 实现桌面应用开发，共享 CEF 运行时](https://docs.deno.com/runtime/desktop/) ⭐️ 8.0/10

Deno Desktop 随 Deno v2.9.0（当前为 canary 版本）发布，允许开发者使用 Deno 构建桌面应用，支持 CEF、Webview 和 Raw 等多种渲染后端，并计划推出共享 CEF 运行时，将二进制体积降至几 MB。 这扩展了 Deno 生态系统至桌面开发领域，通过共享运行时提供了 Electron 的轻量级替代方案，可显著减少磁盘占用并简化基于 Deno 的桌面应用分发。 共享 CEF 运行时已在路线图中；目前每个应用仍捆绑自己的 CEF 副本。编译时授予的权限会固化到二进制文件中，社区建议在运行时向用户展示权限信息。

hackernews · GeneralMaximus · 6月22日 05:38 · [社区讨论](https://news.ycombinator.com/item?id=48626137)

**背景**: Deno 是一个基于 Rust 和 V8 构建的现代 JavaScript 和 TypeScript 运行时。Chromium Embedded Framework (CEF) 允许在应用中嵌入 Chromium 浏览器。Deno Desktop 使用 CEF 或 Webview 渲染 UI，类似于 Electron，但通过共享运行时实现更小的体积。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.deno.com/runtime/desktop/">Desktop apps | Deno Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Chromium_Embedded_Framework">Chromium Embedded Framework - Wikipedia</a></li>
<li><a href="https://github.com/chromiumembedded/cef">GitHub - chromiumembedded/ cef : Chromium Embedded Framework ...</a></li>

</ul>
</details>

**社区讨论**: 社区对 Deno Desktop 感到兴奋，称赞其减小二进制体积和改善权限处理的潜力。部分用户希望像 WebUI 一样提供“在浏览器中启动”选项，另一些用户则讨论了共享 CEF 运行时的版本管理挑战。

**标签**: `#Deno`, `#Desktop`, `#CEF`, `#Webview`, `#Runtime`

---

<a id="item-11"></a>
## [Claude Code 的扩展思考输出是有损摘要](https://patrickmccanna.net/the-text-in-claude-codes-extended-thinking-output-is-not-authentic/) ⭐️ 8.0/10

一项分析揭示，Claude Code 的“扩展思考”模式中显示的文本并非模型的实际推理过程，而是其有损摘要，这意味着原始的思维链对用户隐藏。 这引发了对 AI 透明度的严重担忧，因为用户无法验证模型的推理过程或检测隐藏的提示注入，同时也凸显了主要 AI 公司之间的竞争保密做法。 这种有损摘要被比作将无损的 BMP 转换为有损的 JPEG 再转换回来，导致数据丢失；隐藏的推理还允许模型在隐藏阶段调用函数，可能泄露数据。

hackernews · 0o_MrPatrick_o0 · 6月22日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=48630535)

**背景**: 思维链推理是一种 AI 模型展示其逐步思考过程的技术。包括 Anthropic、OpenAI 和 Google 在内的许多 AI 公司会模糊或总结这种推理过程，以保护专有方法并防止竞争对手利用其思维链进行训练，但这同时也降低了透明度和安全性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/visible-extended-thinking">Claude 's extended thinking \ Anthropic</a></li>
<li><a href="https://claudecodeguides.com/claude-code-extended-thinking-skills-integration-guide/">Extended Thinking + Claude Skills (2026) | Claude Code Guides</a></li>
<li><a href="https://www.claudecodecamp.com/p/claude-code-extended-thinking">Claude Code Extended Thinking</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对隐藏推理的强烈不信任，警告称这可能导致秘密提示注入和数据泄露。一些人指出，出于竞争原因，所有主要 AI 公司都普遍采用这种做法，而另一些人则认为这些推理块可能根本不像人类的思考方式。

**标签**: `#AI transparency`, `#hidden reasoning`, `#Claude Code`, `#security`, `#LLM`

---

<a id="item-12"></a>
## [本地运行 GLM-5.2：MoE 卸载指南](https://unsloth.ai/docs/models/glm-5.2) ⭐️ 7.0/10

Unsloth 发布了使用 MoE 卸载技术本地运行 GLM-5.2 的指南，需要 24GB 显存和 256GB 内存，并提供量化选项以减少内存占用。 这使得爱好者和研究人员能够在消费级硬件上运行最先进的开源模型，可能减少对云 API 的依赖，并引发关于硬件可行性和量化权衡的讨论。 该指南指出动态 4 位和 5 位量化（UD-Q4_K_XL 和 UD-Q5_K_XL）通常无损，但社区评论指出提示处理速度可能比纯 GPU 设置慢 20-50 倍，使得没有昂贵 GPU 的情况下实时使用不切实际。

hackernews · TechTechTech · 6月22日 21:21 · [社区讨论](https://news.ycombinator.com/item?id=48636377)

**背景**: GLM-5.2 是一个拥有数千亿参数的混合专家（MoE）大模型，需要大量内存。MoE 卸载技术通过在 GPU 和系统内存之间交换专家权重来运行此类模型，以速度换取内存。量化降低模型精度以减少内存使用，但可能影响输出质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://unsloth.ai/docs/models/glm-5.2">GLM - 5 . 2 - How to Run Locally | Unsloth Documentation</a></li>
<li><a href="https://insiderllm.com/guides/run-glm-5-2-locally/">How to Run GLM 5 . 2 Locally: GPU, VRAM & Quant Guide | InsiderLLM</a></li>
<li><a href="https://arxiv.org/abs/2312.17238">Fast Inference of Mixture-of-Experts Language Models with Offloading</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了复杂情绪：一些拥有高端硬件（如 192GB 内存+RTX 3090）的用户认为要求几乎可以达到，而另一些用户则强调卸载和量化带来的严重速度惩罚，质疑实际可用性。还有关于本地模型是否正在缩小与云 API 的差距、可能威胁云提供商的争论。

**标签**: `#LLM`, `#local deployment`, `#quantization`, `#MoE`, `#hardware`

---

<a id="item-13"></a>
## [Oak：面向 AI 代理的 Git 替代品](https://oak.space/oak/oak) ⭐️ 7.0/10

Oak 是一个专为 AI 代理设计的新型版本控制系统，它通过虚拟挂载技术让代理无需下载完整仓库即可工作，支持并行任务执行并减少令牌消耗。 这很重要，因为 AI 代理经常面临 Git 仓库体积大和顺序工作流的挑战，Oak 的方法通过最小化数据传输和令牌消耗，有望显著提升代理效率并降低成本。 Oak 仍处于早期开发阶段，缺少 Windows 支持、CI、问题跟踪和评论功能，但团队已将其作为主要版本控制系统使用数月，没有 Git 备份。虚拟挂载类似于 Google 的 google3 方法和微软的 VFS for Git。

hackernews · zdgeier · 6月22日 15:37 · [社区讨论](https://news.ycombinator.com/item?id=48631726)

**背景**: 像 Git 这样的版本控制系统会随时间跟踪文件变更，但需要下载完整的仓库历史，这对 AI 代理来说可能体积庞大且速度缓慢。AI 代理通常需要并行处理多个任务，而 Git 的 worktree 功能使用起来很繁琐。虚拟挂载允许按需获取文件，从而减少存储和带宽消耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hypestkey.com/iso-mastery-unlocking-windows-10-disk-image-files-like-a-pro/">How to Mount ISO Files in Windows 10: Expert Virtual Drive Guide</a></li>
<li><a href="https://www.youtube.com/watch?v=v-bz365fqq4">create and mount virtual disk VHD file using Diskpart... - YouTube</a></li>
<li><a href="https://mundobytes.com/en/Mount-virtual-drives-in-Windows-with-mountvol-and-subst/">Mounting virtual drives with mountvol and subst in Windows</a></li>

</ul>
</details>

**社区讨论**: 社区评论既表达了兴趣也提出了质疑。一些用户称赞懒加载挂载概念具有创新性，并将其与 Google 的内部系统进行比较，而另一些用户则质疑在 Git 已经普及且 AI 模型已熟悉 Git 的情况下，是否有必要开发新的 VCS。讨论还涉及放弃 Git 生态系统的权衡。

**标签**: `#version control`, `#AI agents`, `#developer tools`, `#git alternative`

---

<a id="item-14"></a>
## [Xfce Wayland 合成器 xfwl4 首个预览版发布](https://lwn.net/Articles/1078942/) ⭐️ 7.0/10

Brian Tarricone 宣布了 xfwl4 的首个预览版发布，这是为 Xfce 桌面环境开发的全新 Wayland 合成器，历时近六个月。 这标志着 Xfce 从 X11 向 Wayland 过渡的重要里程碑，确保这一轻量级桌面环境在现代 Linux 生态中保持竞争力。 xfwl4 使用 Rust 语言从头编写，并基于 Smithay 库，而非基于现有的 xfwm4 代码。其目标是尽可能复现 Xfce 在 X11 下的体验。

rss · LWN.net · 6月22日 13:44

**背景**: Wayland 是一种现代显示服务器协议，旨在取代老旧的 X11 系统，提供更好的性能和安全性。Xfce 是 Linux 上流行的轻量级桌面环境。向 Wayland 过渡是许多桌面环境的重要任务，Xfce 的这一举措是这一持续转变中的关键一步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://itsfoss.gitlab.io/post/xfce-brand-new-wayland-compositor-xfwl4/">Xfce Is Getting a Brand-New Wayland Compositor Called Xfwl 4</a></li>
<li><a href="https://www.phoronix.com/news/Xfce-Xfwl4-Wayland">Xfwl 4 Being Developed As New Wayland Compositor For... - Phoronix</a></li>

</ul>
</details>

**标签**: `#Wayland`, `#Xfce`, `#Linux Desktop`, `#Compositor`

---

<a id="item-15"></a>
## [OSPM 2026 第一天：空闲状态、sched_ext 和锁持有者抢占](https://lwn.net/Articles/1077759/) ⭐️ 7.0/10

OSPM 2026 Linux 内核峰会第一天涵盖了空闲状态选择、通过 sched_ext 实现用户空间调度器以及锁持有者抢占等主题的讨论。 这些讨论直接影响 Linux 内核的电源管理和调度性能，从而影响从嵌入式设备到数据中心等广泛用户的系统效率和响应能力。 峰会于四月中旬在英国剑桥举行，会议摘要随后在 LWN 上发布。主题包括空闲状态选择的改进、可扩展调度器类 sched_ext 以及解决锁持有者抢占问题。

rss · LWN.net · 6月22日 13:26

**背景**: OSPM（Linux 内核电源管理与调度峰会）是一个专注于 Linux 内核电源管理和调度的年度会议。空闲状态选择控制 CPU 如何进入低功耗状态，sched_ext 允许将调度器编写为 BPF 程序，而锁持有者抢占是指持有锁的线程被抢占，导致效率低下。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kernel.org/doc/html/next/scheduler/sched-ext.html">Extensible Scheduler Class — The Linux Kernel documentation</a></li>
<li><a href="https://www.kernel.org/doc/html/latest/driver-api/pm/cpuidle.html">CPU Idle Time Management — The Linux Kernel documentation</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#power management`, `#scheduling`, `#sched_ext`, `#OSPM`

---

