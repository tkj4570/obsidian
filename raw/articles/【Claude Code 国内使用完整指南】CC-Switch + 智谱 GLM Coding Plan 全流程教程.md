---
title: "【Claude Code 国内使用完整指南】CC-Switch + 智谱 GLM Coding Plan 全流程教程"
source: "https://blog.csdn.net/weixin_44262492/article/details/160348230"
author:
  - "[[weixin_44262492]]"
published: 2026-04-20
created: 2026-06-23
description: "文章浏览阅读7.2k次，点赞21次，收藏25次。Claude Code国内使用方案：CC-Switch+智谱GLM组合教程 本文详细介绍如何在国内使用Claude Code的替代方案——CC-Switch+智谱GLM Coding Plan组合。该方案无需信用卡和代理，费用仅为官方Claude Pro的1/7，提供3倍使用额度。 主要内容包括： 智谱GLM Coding Plan的申请流程（注册、实名认证、套餐选择） API Key的获取方法 CC-Switch工具的下载安装指南（支持Windows/macOS/Linux） 配置使用全流程，包含详细的图_cc switch glm"
tags:
  - "clippings"
---
## Claude Code 国内使用完整指南：CC- Switch + 智谱 GLM Coding Plan 全流程教程

**亲爱的朋友们，创作不容易，若对您有帮助的话，请点赞收藏加关注哦，您的关注是我持续创作的动力，谢谢大家！有问题请私信或联系邮箱：jasonai.fn@gmail.com**

Claude Code 是目前公认最强的 AI 编程助手，但官方订阅需要信用卡支付、访问有地区限制、$20/月的 Claude Pro 性价比也有限。对于国内开发者， **CC-Switch + 智谱 GLM Coding Plan** 是目前口碑最好的组合：配置最简单、费用约为官方的 1/7、额度是 Claude Pro 的 3 倍，且无需代理。

本文将完整还原： **智谱 Coding Plan 申请 → API Key 获取 → CC-Switch 安装配置 → 验证上手** 的全过程，每一步都有截图描述，零基础可跟做。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/378ac8690c084c718cea0079e41eb700.png)

---

### 一、整体方案架构说明

在动手之前，先理解这套方案是怎么工作的，有助于遇到问题时快速定位。

```
┌─────────────────────────────────────────────────────────┐
│                    你的本机终端                           │
│                                                         │
│   claude 命令                                            │
│      ↓                                                  │
│   CC-Switch（读取配置，注入 API Key + Endpoint）          │
│      ↓                                                  │
│   智谱 Coding API Endpoint                               │
│    https://open.bigmodel.cn/api/anthropic           │
│      ↓                                                  │
│   智谱 GLM 模型（GLM-5.1 / GLM-5-Turbo / GLM-4.7）      │
│                                                         │
│   ✅ 无需代理  ✅ 国内直连  ✅ 稳定不封号                  │
└─────────────────────────────────────────────────────────┘
text1234567891011121314
```

| 组件 | 作用 |
| --- | --- |
| **CC-Switch** | 桌面 GUI 工具，管理 Claude Code 的 API 配置，免去手动改配置文件 |
| **智谱 GLM Coding Plan** | 国内 AI 大模型平台，提供 Claude Code 兼容的 OpenAI 格式 API 中转 |
| **GLM 模型** | GLM-5.1（对标 Claude Opus）、GLM-5-Turbo（对标 Claude Sonnet） |

---

### 二、第一步：申请 智谱 GLM Coding Plan

#### 2.1 注册智谱 AI 账号

**Step 1 — 访问官网**

打开 [https://open.bigmodel.cn](https://open.bigmodel.cn/) ，点击右上角"注册"。

**Step 2 — 完成注册**

- 使用手机号注册，填写验证码
- 设置密码后登录

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/aaa1b701164143dbb7efa568e2232fd2.png)

**Step 3 — 实名认证（必须）**

进入控制台后，根据提示完成实名认证（身份证），认证后才能订阅套餐和生成 API Key。认证通常在几分钟内完成。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4a340dff9c3e4b00a6d4e731dfe58623.png)

---

#### 2.2 订阅 GLM Coding Plan

**Step 1 — 进入套餐页面**

登录后，访问 [https://docs.bigmodel.cn/cn/coding-plan/overview](https://docs.bigmodel.cn/cn/coding-plan/overview) ，或在控制台顶部导航点击 **“Coding Plan”** / **“套餐”** 。

**Step 2 — 了解套餐选项**

| 套餐 | 月费 | 适合人群 | 每日额度特点 |
| --- | --- | --- | --- |
| **Lite** | ¥20/月 | 轻度使用、学生、探索期 | 基础额度，5小时周期恢复 |
| **Pro** | 约 ¥60/月 | 日常编程、中频使用 | 额度约 Lite 的 3 倍 |
| **Max** | 约 ¥120/月 | 重度编程、专业开发者 | 最高额度，高峰期优先 |

> **新手推荐** ：先购买 **Lite 月套餐（¥20）** 试用，确认效果后再考虑升级或年付（年付通常有 7 折优惠）。
> 
> **优惠提示** ：新用户首次购买季付套餐可享 **5 折** 优惠，Lite 套餐低至 **¥48/季** （约 ¥16/月）。  
> ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8c3939a6c5bf4977b3094bddeba41c69.png)

**Step 3 — 完成支付**

选择套餐 → 确认购买 → 支付宝/微信支付，到账即时生效。

---

#### 2.3 获取 API Key

**Step 1 — 进入 API Key 管理页**

在控制台左侧导航找到 **“API Keys”** 或 **“密钥管理”** ，也可直接访问：  
[https://open.bigmodel.cn/usercenter/apikeys](https://open.bigmodel.cn/usercenter/apikeys)

**Step 2 — 创建新 Key**

点击 **“新建 API Key”** → 填写名称（如 `claude-code-key` ）→ 点击确认。

**Step 3 — 复制保存 Key**

Key 格式类似： `a1b2c3d4e5f6...`（一长串字母数字组合）

> ⚠️ **Key 只会完整显示一次** ，创建后立即复制并妥善保存！遗失需重新创建。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/837ee6c1f5df4e479c51f6d432adab85.png)

**Step 4 — 记录 Coding 专用端点**

智谱为 Coding Plan 提供了专用 API 端点，与通用端点不同：

```
Coding 专用端点（Claude Code 使用这个）：
https://open.bigmodel.cn/api/anthropic

通用端点（普通 API 调用）：
https://open.bigmodel.cn/api/paas/v4
12345
```

> ⚠️ 两个端点 **不可混用** ，CC-Switch 配置智谱时填写 Coding 专用端点。

---

### 三、第二步：安装 CC-Switch

#### 3.1 什么是 CC-Switch

CC-Switch 是开源的跨平台桌面工具（GitHub: [farion1231/cc-switch](https://github.com/farion1231/cc-switch) ），专门用来管理 Claude Code 等 AI 编程工具的 API 配置。它解决了一个核心痛点： **不用手动改配置文件或设置环境变量** ，在 GUI 界面里点一下就能切换 API 提供商。

核心功能一览：

| 功能 | 说明 |
| --- | --- |
| **一键切换供应商** | 在官方 Anthropic / 智谱 / DeepSeek / Kimi 等之间秒切 |
| **API Key 管理** | 集中管理多个 Key，不用记在哪个文件里 |
| **健康检查** | 一键测试 API 连通性和延迟 |
| **用量统计** | 查看 Token 消耗、缓存命中率、按模型分类的费用 |
| **MCP 管理** | 可视化增删 MCP 服务器，配置自动同步 |
| **Skills 管理** | 安装增强 Claude Code 能力的提示词插件 |
| **多应用支持** | 同时管理 Claude Code、Codex、Gemini CLI 等 |

---

#### 3.2 下载 CC-Switch

前往 GitHub Release 页面下载：  
**[https://github.com/farion1231/cc-switch/releases](https://github.com/farion1231/cc-switch/releases)**

根据你的操作系统选择对应文件：

| 系统 | 下载文件 | 说明 |
| --- | --- | --- |
| **Windows 安装版** | `CC-Setup-x.x.x.exe` | 推荐，自动创建快捷方式 |
| **Windows 便携版** | `CC-windows-x.x.x.zip` | 解压即用，无需安装 |
| **macOS** | `CC-Switch-vX.X.X-macOS.zip` | 解压后拖入 Applications |
| **Linux** | `CC-Switch-vX.X.X-linux.AppImage` | 给予执行权限后运行 |

> 下载页面在 Assets 折叠区，如果看不到文件列表点击 “Assets” 展开。

---

#### 3.3 安装 CC-Switch

**Windows（安装版）** ：

1. 双击下载的 `.exe` 文件
2. 如果弹出"Windows 已保护你的电脑"提示，点击"更多信息" → “仍要运行”
3. 按照安装向导默认选项完成安装
4. 桌面或开始菜单找到 CC-Switch 图标，双击启动

**macOS** ：

1. 解压 `.zip` 文件，得到 `CC-Switch.app`
2. 将 `CC-Switch.app` 拖入 `/Applications` 文件夹
3. 首次打开时，如果提示"无法验证开发者"，进入 **系统设置 → 隐私与安全性** ，点击"仍要打开"
4. 或在终端运行：
	```bash
	sudo xattr -rd com.apple.quarantine /Applications/CC-Switch.app
	bash1
	```

---

### 四、第三步：在 CC-Switch 中配置智谱

#### 4.1 认识 CC-Switch 主界面

首次启动 CC-Switch 后，界面主要分为以下区域：

```
┌──────────────────────────────────────────────────┐
│  [Claude Code] [Codex] [Gemini CLI]  ← 应用切换栏 │
├──────────────────────────────────────────────────┤
│  供应商列表                     [+ 添加供应商]     │
│  ○ Anthropic 官方               [启用] [健康检查]  │
│  ○ 智谱 GLM（待配置）            [启用] [健康检查]  │
│  ...                                             │
├──────────────────────────────────────────────────┤
│  [供应商] [用量] [MCP] [Skills] [设置]  ← 底部导航 │
└──────────────────────────────────────────────────┘
text12345678910
```

#### 4.2 添加智谱供应商

**Step 1 — 确认当前管理的是 Claude Code**

界面顶部应用切换栏，确认选中的是 **Claude Code** 图标（Claude 的 logo）。

**Step 2 — 点击添加供应商**

点击右上角的 **“+”** 按钮，弹出添加供应商界面。

**Step 3 — 选择智谱预设（或手动填写）**

在内置预设列表中找到 **“智谱 AI”** / **“GLM”** ，点击选中。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/53bf955165a34982af7fb9c437ec5fd0.png)

> 如果预设列表中没有智谱，选择"自定义"手动填写：

| 字段 | 填写内容 |
| --- | --- |
| **供应商名称** | 智谱 GLM Coding |
| **API Base URL** | `https://open.bigmodel.cn/api/anthropic` |
| **API Key** | 粘贴你从智谱控制台复制的 Key |
| **模型（大模型/Opus 对应）** | `glm-5.1` |
| **模型（中等/Sonnet 对应）** | `glm-5-turbo` |
| **模型（小模型/Haiku 对应）** | `glm-4.7` |

**Step 4 — 保存配置**

点击"保存"或"确认"，供应商出现在列表中。

---

#### 4.3 启用智谱供应商

**Step 1 — 在供应商列表中找到刚添加的智谱 GLM**

**Step 2 — 点击"健康检查"**

CC-Switch 会发送一个测试请求，验证：

- API Key 是否有效
- Coding 端点是否可达
- 响应延迟是多少

健康检查通过后会显示绿色"✅ 正常"，失败则显示具体错误信息。

**Step 3 — 点击"启用"**

点击"启用"按钮，CC-Switch 会自动将配置写入 Claude Code 的配置文件， **不需要手动设置任何环境变量** 。

当前激活的供应商会有高亮标识（如橙色圆点或"当前"标签）。

---

#### 4.4 验证配置生效

打开终端（Mac: Terminal / Windows: PowerShell 或 CMD），运行：

```bash
claude "用一句话介绍你自己"
bash1
```

如果返回 GLM 模型的回复（内容中可能提到"智谱"或"GLM"），说明配置成功。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0f5a2421dc744490821d274827ac033d.png)

也可以运行：

```bash
claude doctor
bash1
```

在输出中找到 `API Provider` 或 `Base URL` 字段，确认显示的是智谱的 Coding 端点。

---

### 五、模型选择与使用建议

#### 5.1 智谱模型对应关系

| 智谱模型 | 对标 Claude 模型 | 适用场景 | 额度消耗系数 |
| --- | --- | --- | --- |
| **GLM-5.1** | Claude Opus | 复杂推理、架构设计、难题调试 | 高峰期 3×，非高峰期 2× |
| **GLM-5-Turbo** | Claude Sonnet | 日常编程、代码补全、文档生成 | 标准 1× |
| **GLM-4.7** | Claude Haiku | 简单问答、快速响应、轻量任务 | 标准 1× |
| **GLM-4.5-Air** | — | 极速响应，适合高频简单任务 | 最低 |

> **额度节省建议** ：日常编程任务用 GLM-5-Turbo，遇到真正复杂的架构问题再切换到 GLM-5.1。高峰期（每天 14:00–18:00 UTC+8）GLM-5.1 消耗额度是平时的 1.5 倍，建议避开高峰期处理重型任务。

#### 5.2 在 CC-Switch 中切换模型

CC-Switch 支持 4 级模型配置（对应 Claude Code 内部的 Haiku / Sonnet / Opus / 自定义），在供应商配置页可以分别指定每个级别使用哪个 GLM 模型，Claude Code 会根据任务复杂度自动选用不同级别。

#### 5.3 额度恢复机制

当套餐额度耗尽时， **不会** 自动扣费账户余额，而是等待下一个 **5 小时周期** 自动恢复。规划好使用节奏，避免在关键时刻额度归零。

---

### 六、CC-Switch 进阶功能

#### 6.1 用量统计

点击底部导航的 **“用量”** 标签，可以看到：

- 各供应商的 Token 消耗明细
- 缓存命中率（影响实际费用）
- 按模型分类的费用估算
- 历史用量趋势

#### 6.2 MCP 服务器管理

点击 **“MCP”** 标签，可以可视化添加、编辑、删除 MCP 服务器，配置自动同步到 Claude Code。智谱 Coding Plan 套餐本身也内置了若干 MCP 权益（如联网搜索、网页读取、开源仓库 MCP）。

#### 6.3 Skills 安装

Skills 是增强 Claude Code 能力的提示词插件（类似 Claude Code 的 Skill 系统）。点击 **“Skills”** → 安装预设仓库中的 Skills，或从 GitHub URL 安装自定义 Skills。

#### 6.4 快速切换供应商（热切换）

CC-Switch 支持 **无需重启 Claude Code** 的热切换——在供应商列表中点击另一个供应商的"启用"，配置立即生效，正在运行的 Claude Code 会话自动使用新配置。

---

### 七、常见问题排查

| 问题现象 | 原因 | 解决方案 |
| --- | --- | --- |
| 健康检查失败：“401 Unauthorized” | API Key 错误或未激活套餐 | 检查 Key 是否完整复制；确认已购买 Coding Plan 套餐 |
| 健康检查失败：“404 Not Found” | Endpoint 填写了通用端点 | 改为 Coding 专用端点： `https://open.bigmodel.cn/api/coding/paas/v4` |
| `claude` 命令仍然连接官方 API | 系统环境变量覆盖了 CC-Switch 配置 | 检查是否设置了 `ANTHROPIC_API_KEY` 或 `ANTHROPIC_BASE_URL` 环境变量，删除后重试 |
| CC-Switch 安装后 Mac 提示"无法打开" | Gatekeeper 拦截 | 系统设置 → 隐私与安全性 → 点击"仍要打开"；或运行 `sudo xattr -rd com.apple.quarantine /Applications/CC-Switch.app` |
| 额度消耗过快 | 高峰期大量使用 GLM-5.1 | 日常任务切换到 GLM-5-Turbo；避开 14:00–18:00（UTC+8）高峰期 |
| 模型回复质量不如预期 | 使用了较轻量的模型 | 在 CC-Switch 供应商配置中将 Opus 级别改为 `glm-5.1` |
| 响应速度慢 | 网络抖动 | 点击"健康检查"查看延迟；智谱 API 国内直连，通常延迟 < 300ms |

---

### 八、方案对比：为什么选择智谱 + CC-Switch

| 维度 | 官方 Claude Pro | 智谱 GLM Coding Plan |
| --- | --- | --- |
| **月费** | $20（约 ¥145） | ¥20 起（约 1/7） |
| **额度** | 有限制，高频使用受限 | 约官方 3 倍 |
| **地区** | 需代理，有封号风险 | 国内直连，稳定 |
| **支付方式** | 信用卡（Visa/Mastercard） | 支付宝、微信 |
| **模型** | Claude Opus 4 / Sonnet 4 | GLM-5.1 / GLM-5-Turbo |
| **配置难度** | 简单 | CC-Switch 图形化，同样简单 |
| **多工具支持** | 仅 Claude Code | Claude Code + Codex + Kilo Code 等 10+ |

---

### 九、总结

| 步骤 | 操作 | 关键点 |
| --- | --- | --- |
| **① 注册智谱** | [open.bigmodel.cn](https://open.bigmodel.cn/) 注册并实名 | 实名认证后才能订阅 |
| **② 购买套餐** | 选择 Lite（¥20）起步 | 新用户季付可享 5 折 |
| **③ 获取 Key** | 控制台创建 API Key | Key 只显示一次，立即保存 |
| **④ 安装 CC-Switch** | GitHub Release 下载对应系统包 | Mac 需解除 Gatekeeper 限制 |
| **⑤ 配置供应商** | 填入 Coding 端点 + API Key | 端点必须用 Coding 专用 URL |
| **⑥ 启用验证** | 健康检查绿灯后点击启用 | `claude "hello"` 验证生效 |

**CC-Switch + 智谱 GLM Coding Plan** 是目前国内使用 Claude Code 性价比最高、配置最简单的方案。¥20/月就能解锁 AI 编程助手的完整能力，无需代理，直接在终端里 `claude` 开始工作。

---

**参考资料** ：

1. [CC-Switch GitHub 主仓库 — farion1231](https://github.com/farion1231/cc-switch)
2. [CC-Switch 中文说明文档](https://github.com/farion1231/cc-switch/blob/main/README_ZH.md)
3. [智谱 AI GLM Coding Plan 套餐概览](https://docs.bigmodel.cn/cn/coding-plan/overview)
4. [智谱 AI 开放平台](https://open.bigmodel.cn/)
5. [菜鸟教程 — CC Switch 一键切换 API](https://www.runoob.com/ai-agent/cc-switch.html)
6. [知乎 — 最强编程模型 Claude Code 国内使用指南](https://zhuanlan.zhihu.com/p/1996316309248575298)