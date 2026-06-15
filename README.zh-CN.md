🌐 语言选择: [English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md) | [Español](./README.es.md) | [Deutsch](./README.de.md) | [Français](./README.fr.md) | [日本語](./README.ja.md) | [한국어](./README.ko.md) | [Türkçe](./README.tr.md) | [Русский](./README.ru.md)

[![EvoLinkAI Banner](./assets/banner.png)](https://evolink.ai/signup?utm_source=github&utm_medium=banner&utm_campaign=awesome-openclaw-skills)

# awesome-openclaw-skills-for-real-work 🐙

> **质量优先于数量。** 这不是 ClawHub 上所有技能的镜像，而是一份精选指南，只收录真正能在实际工作流中使用的技能 — 经过测试、整理，并且配有清晰的使用说明。

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![ClawHub](https://img.shields.io/badge/powered%20by-ClawHub-blue)](https://clawhub.com)
[![OpenClaw](https://img.shields.io/badge/runtime-OpenClaw-purple)](https://openclaw.ai)
![Total Skills](https://img.shields.io/badge/total%20skills-80-brightgreen)

---

## 设计理念

大多数技能列表只是简单的内容堆砌，这个列表不一样：
- ✅ **每个条目都经过人工审核** — 不是从注册表自动抓取的
- ✅ **包含完整文档** — 每个技能在 `./skills/` 目录下都有详细的使用指南
- ✅ **优先考虑实用性** — 如果不能帮你更快交付产品或者提升思考效率，就不会出现在这里
- ✅ **如实告知局限性** — 安全标记和 API 密钥要求都会明确标注
- ✅ **支持组合使用** — 技能组合起来使用效果最好（参见 [入门套装](#-入门套装)）

---

## 符号说明

| 标记 | 含义 |
|-------|---------|
| 🆓 无需 API 密钥 | 开箱即用 — 不需要外部凭证 |
| 🔑 需要 API 密钥 | 需要外部服务的密钥才能使用 |
| ⚠️ 安全标记 | ClawHub 安全扫描发现潜在问题 — 安装前请仔细审核 |
| ⭐ 星标 | ClawHub 社区星标数量 |
| 📖 完整文档 | 本仓库包含详细的使用文档 |

---

## 目录

- [🚀 入门套装](#-入门套装)
- [🔍 研究与搜索](#-研究与搜索)
- [🤖 浏览器与自动化](#-浏览器与自动化)
- [🧠 记忆与知识管理](#-记忆与知识管理)
- [💬 通讯与消息](#-通讯与消息)
- [📊 数据与文档处理](#-数据与文档处理)
- [🛠️ 开发工具](#️-开发工具)
- [🎨 创意与媒体](#-创意与媒体)
- [💰 金融与市场](#-金融与市场)
- [🏠 智能家居与系统](#-智能家居与系统)
- [🔒 安全](#-安全)
- [⚡ Agent 核心能力](#-agent-核心能力)
- [所有技能索引](./skills/)
- [贡献指南](#贡献指南)

---

## 🚀 入门套装

> 刚接触 OpenClaw？不要一下子安装 50 个技能，从这里开始。

### 🟢 新手套装 — "10 分钟就能上手"

最低可用的 Agent 配置，完全不需要 API 密钥。

| 技能 | 文档 | 为什么选它 |
|-------|------|-----|
| [记忆配置](./skills/memory-setup.md) 📖 | ✅ | 让 Agent 在会话之间记住你的偏好 |
| [多搜索引擎](./skills/multi-search-engine.md) 📖 | ✅ | 无需密钥的网页搜索 — 所有功能的基础 |
| [内容总结](./skills/summarize.md) 📖 | ✅ | 读更少的内容，理解更多信息 |
| [天气查询](./skills/weather.md) 📖 | ✅ | 快速展示 Agent 能力的实用示例 |
| [Todoist 任务管理](./skills/todoist.md) 📖 | ✅ | 真正好用的任务管理功能 |

---

### 🔵 高级用户套装 — "用一个 Agent 替代 5 个应用"

适合每天都使用 Agent 的用户。

| 技能 | 文档 | 为什么选它 |
|-------|------|-----|
| [自我提升 + 主动型 Agent](./skills/self-improving-agent.md) 📖 | ✅ | Agent 可以永久学习你的偏好 |
| [深度研究专业版](./skills/deep-research-pro.md) 📖 | ✅ | 多来源带引用的研究报告 |
| [Gmail 管理](./skills/gmail.md) 📖 | ✅ | 直接在聊天中处理邮件 |
| [Notion 集成](./skills/notion.md) 📖 | ✅ | 直接写入你的第二大脑 |
| Agent 浏览器 | ❌ | 可视化控制网页操作 |
| [文件系统管理](./skills/filesystem-management.md) 📖 | ✅ | 不用动手就能管理文件和文件夹 |

---

### 🟠 开发者套装 — "编码、发布、循环迭代"

为想要一个带真实工具的 AI 结对程序员的工程师打造。

| 技能 | 文档 | 为什么选它 |
|-------|------|-----|
| [Git 基础操作](./skills/git-essentials.md) 📖 | ✅ | 在聊天中完成提交、分支、对比差异等操作 |
| [Docker 基础操作](./skills/docker-essentials.md) 📖 | ✅ | 不用记命令就能管理容器 |
| [GitHub 集成](./skills/github.md) 📖 | ✅ | 完全控制 Issue、PR、仓库 |
| [Tmux 终端复用](./skills/tmux.md) 📖 | ✅ | 持久化终端会话，断开连接也不会丢失 |
| [安全审计工具](./skills/security-auditor.md) 📖 | ✅ | 在发布前发现问题 |
| [n8n 工作流自动化](./skills/n8n-workflow-automation.md) 📖 | ✅ | 用 AI 构建自动化流水线 |

---

### 🟣 研究员套装 — "比房间里所有人知道的都多"

适合分析师、作家和任何需要基于信息做决策的人。

| 技能 | 文档 | 为什么选它 |
|-------|------|-----|
| [深度研究专业版](./skills/deep-research-pro.md) 📖 | ✅ | 带引用的多来源深度研究 |
| [Brave 搜索](./skills/brave-search.md) 📖 | ✅ | 快速、私密、实时的网页搜索结果 |
| Tavily 搜索 | ❌ | AI 优化的搜索结果 |
| [新闻摘要](./skills/news-summary.md) 📖 | ✅ | 自动化的每日简报 |
| [内容总结](./skills/summarize.md) 📖 | ✅ | 长文档一键提取核心要点 |
| [Obsidian 集成](./skills/obsidian.md) 📖 | ✅ | 直接将研究结果保存到你的知识库 |

---

### 🔴 内容创作者套装 — "产出更多，思考更少"

适合营销人员、社交媒体运营和写作者。

| 技能 | 文档 | 为什么选它 |
|-------|------|-----|
| [AI 文本人性化](./skills/humanize-ai-text.md) 📖 | ✅ | 让 AI 生成的内容听起来更自然 |
| SuperDesign | ❌ | UI/设计规范和原型描述 |
| [OpenAI 图片生成](./skills/openai-image-gen.md) 📖 | ✅ | 在聊天中直接生成图片 |
| [Markdown 转换器](./skills/markdown-converter.md) 📖 | ✅ | 任意格式和 Markdown 之间互转 |
| [YouTube 内容提取](./skills/youtube-watcher.md) 📖 | ✅ | 不用看视频就能完成研究 |
| 小红书自动化 ⚠️ | ❌ | 小红书内容工作流 |

---

## 🔍 研究与搜索

任何高效 Agent 的基础，选一个主搜索引擎，再按需添加专业搜索引擎。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [多搜索引擎](./skills/multi-search-engine.md) 📖 | 297 | 🆓 | ✅ | 一次调用整合多个引擎 — 最佳默认搜索技能 |
| [Brave 搜索](./skills/brave-search.md) 📖 | 149 | 🔑 | ✅ | 快速、私密、可靠 — 信噪比极佳 |
| [深度研究专业版](./skills/deep-research-pro.md) 📖 | 45 | 🆓 | ✅ | 多来源研究，输出结构化带引用的报告 |
| [Exa 网页搜索（免费版）](./skills/exa-web-search.md) 📖 | 57 | 🆓 | ✅ | 神经搜索 — 查找语义相关页面，不只是关键词匹配 |
| Tavily 搜索 | 77 | 🔑 | ❌ | AI 原生搜索 API，非常适合研究工作流 |
| Tavily AI 搜索 | 26 | 🔑 ⚠️ | ❌ | 替代的 Tavily 集成 — 安装前请审核安全扫描结果 |
| DuckDuckGo 网页搜索 | 10 | 🆓 | ❌ | 简单、注重隐私、无需 API 密钥 |
| [Searxng](./skills/searxng.md) 📖 | 22 | 🆓 | ✅ | 自托管元搜索引擎 — 需要你自己的 SearXNG 实例 |
| 百度网页搜索 | 112 | 🔑 | ❌ | 中文网页搜索 |
| [新闻摘要](./skills/news-summary.md) 📖 | 78 | 🆓 | ✅ | 自动化每日新闻摘要 |
| Answer Overflow | 123 | 🆓 | ❌ | 搜索 Discord 开发者社区的技术答案 |

> **选择建议：** 多搜索引擎（无需密钥，覆盖面广）→ Brave 搜索（质量最佳，需要密钥）→ Exa（语义搜索，免费套餐）

---

## 🤖 浏览器与自动化

这些技能让你的 Agent 真正能在网页上**执行操作**，而不只是查找信息。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| Agent 浏览器 | 64 | 🆓 | ❌ | 可视化浏览器控制 — 点击、输入、截图、爬取 |
| Playwright MCP | 88 | 🆓 | ❌ | 通过 MCP 调用 Playwright — 精准的浏览器自动化 |
| Playwright（自动化 + MCP + 爬虫） | 18 | 🆓 | ❌ | 全套功能：用 Playwright 实现自动化、测试和爬取 |
| [桌面控制](./skills/desktop-control.md) 📖 ⚠️ | 214 | 🆓 | ✅ | 鼠标、键盘、屏幕控制 — 功能强大，但安装前请审核安全扫描结果 |
| 小红书自动化 | 79 | 🆓 ⚠️ | ❌ | 通过 MCP 实现小红书内容工作流 |
| [YouTube 内容提取](./skills/youtube-watcher.md) 📖 | 217 | 🆓 | ✅ | 从 YouTube 视频中提取字幕、摘要和洞察 |
| [Camsnap 摄像头拍照](./skills/camsnap.md) 📖 | 7 | 🆓 | ✅ | 在 macOS 上拍摄摄像头快照 |
| 视频帧提取 | 79 | 🆓 | ❌ | 从本地视频文件中提取帧用于分析 |
| [n8n 工作流自动化](./skills/n8n-workflow-automation.md) 📖 | 88 | 🆓 | ✅ | 从 Agent 中触发和管理 n8n 工作流 |
| [Browser Use](./skills/browser-use.md) 📖 ⚠️ | 65 | 🆓 | ✅ | 浏览器自动化 — 有安全标记，使用前请审核 |

> ⚠️ **Playwright 爬虫技能说明**（⭐38）：有安全标记 — 建议使用 Playwright MCP 替代。

---

## 🧠 记忆与知识管理

没有记忆的 Agent 每次会话都会重置，这些技能让它具备持久化能力。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [记忆配置](./skills/memory-setup.md) 📖 | 83 | 🆓* | ✅ | 基础 — 配置 MEMORY.md 和向量搜索，**从这里开始** |
| [自我提升 + 主动型 Agent](./skills/self-improving-agent.md) 📖 | 384 | 🆓 | ✅ | Agent 从纠正中学习，永久自我反思 |
| [记忆管理器](./skills/memory-manager.md) 📖 | 68 | 🆓* | ✅ | 主动记忆 CRUD — 搜索、更新、删除特定记忆 |
| Agent 记忆 | 14 | 🆓 | ❌ | 轻量级记忆层，适合小型配置 |
| 精英长期记忆 | 131 | 🔑 ⚠️ | ❌ | 高级多层记忆 — 优先审核安全扫描结果 |
| [Obsidian 集成](./skills/obsidian.md) 📖 | 205 | 🆓 | ✅ | 读写 Obsidian 知识库 — 知识底座集成 |
| [Notion 集成](./skills/notion.md) 📖 | 188 | 🔑 | ✅ | Notion 作为 Agent 的外部记忆和工作区 |
| 会话日志 | 15 | 🆓 | ❌ | 自动记录会话，供后续回顾和召回 |
| 本体知识图谱 | 288 | 🆓 | ❌ | 结构化知识图谱 — 构建你的领域语义地图 |

> *向量嵌入（Voyage/OpenAI）可能需要可选的 API 密钥，也有本地提供者可用 — 无需密钥。
>
> **推荐配置：** 记忆配置 → 自我提升 Agent → 记忆管理器

---

## 💬 通讯与消息

你的 Agent 作为通讯中心 — 邮件、团队聊天、任务，全部在一处处理。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [Gmail 管理](./skills/gmail.md) 📖 | 60 | 🔑 | ✅ | 读取、撰写、发送 Gmail — 完整的邮件管理 |
| AgentMail | 45 | 🔑 | ❌ | 带调度和跟进追踪的邮件 Agent |
| [imap-smtp 邮件](./skills/imap-smtp-email.md) 📖 | 56 | 🔑 | ✅ | 通过 IMAP/SMTP 实现通用邮件支持 — 兼容所有服务商 |
| Himalaya | 50 | 🆓 | ❌ | 终端邮件客户端集成 |
| [Slack 集成](./skills/slack.md) 📖 | 91 | 🔑 | ✅ | 发送和读取 Slack 消息，管理频道 |
| [Discord 集成](./skills/discord.md) 📖 | 48 | 🔑 | ✅ | Discord 集成 — 消息、频道、服务器管理 |
| Telegram | 17 | 🔑 | ❌ | 从 Agent 发送 Telegram 消息 |
| Imsg | 16 | 🆓 | ❌ | macOS 上的 iMessage 集成 |
| [Apple 提醒事项](./skills/apple-reminders.md) 📖 | 39 | 🆓 | ✅ | 创建和管理 Apple 提醒事项 — 原生 macOS/iOS 同步 |
| [Todoist 任务管理](./skills/todoist.md) 📖 | 43 | 🔑 | ✅ | 完整的 Todoist 集成 — 任务、项目、优先级 |
| Trello | 106 | 🔑 | ❌ | 在聊天中管理 Trello 看板 |
| [Caldav 日历](./skills/caldav-calendar.md) 📖 | 173 | 🔑 | ✅ | 通过 CalDAV 访问日历 — 兼容 iCloud、Fastmail、Nextcloud |

> **邮件选择：** imap-smtp 适合通用兼容性；如果你只用 Google 服务则选 Gmail
> **任务管理选择：** 高级用户选 Todoist；苹果生态用户选 Apple 提醒事项

---

## 📊 数据与文档处理

不用离开聊天就能读取、写入、转换和分析文档。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [内容总结](./skills/summarize.md) 📖 | 634 | 🆓 | ✅ | 总结任意文本、URL 或文档 — 星标最多的技能之一 |
| [数据分析员](./skills/data-analyst.md) 📖 | 51 | 🆓 | ✅ | 分析数据集，生成洞察，创建图表 |
| 数据分析 | 29 | 🆓 | ❌ | 带代码执行能力的结构化数据分析工作流 |
| [Excel / XLSX 处理](./skills/excel-xlsx.md) 📖 | 40 | 🆓 | ✅ | 读取、写入和操作 Excel 文件 |
| [Word / DOCX 处理](./skills/word-docx.md) 📖 | 62 | 🆓 | ✅ | 创建和编辑 Word 文档 |
| [Nano PDF 阅读器](./skills/nano-pdf.md) 📖 | 147 | 🆓 | ✅ | 轻量级 PDF 阅读器 — 提取速度快，无需 heavy 依赖 |
| [Markdown 转换器](./skills/markdown-converter.md) 📖 | 115 | 🆓 | ✅ | HTML、DOCX、PDF 与 Markdown 格式互转 |
| [AI 文本人性化](./skills/humanize-ai-text.md) 📖 | 144 | 🆓 | ✅ | 重写 AI 生成的内容，使其听起来更自然 |
| Qmd | 75 | 🆓 | ❌ | Quarto Markdown 文档 — 学术和技术出版 |

> ⚠️ **PDF 技能说明**（⭐30, `awspace/pdf`）：有安全标记 — 建议使用 Nano PDF 替代。

---

## 🛠️ 开发工具

面向工程师的技能，假设你知道如何使用。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [GitHub 集成](./skills/github.md) 📖 | 373 | 🔑 | ✅ | Issue、PR、仓库 — 完整的 GitHub API 访问 |
| [Git 基础操作](./skills/git-essentials.md) 📖 | 23 | 🆓 | ✅ | 在聊天中完成提交、分支、合并、对比差异 |
| [Docker 基础操作](./skills/docker-essentials.md) 📖 | 21 | 🆓 | ✅ | 容器管理 — 列表、启动、停止、查看日志 |
| [Tmux 终端复用](./skills/tmux.md) 📖 | 31 | 🆓 | ✅ | 持久化终端会话 — 断开连接也不会丢失 |
| [文件系统管理](./skills/filesystem-management.md) 📖 | 60 | 🆓 | ✅ | 带安全防护的安全文件和文件夹操作 |
| [API 网关](./skills/api-gateway.md) 📖 | 223 | 🔑 | ✅ | 对接 100+ API（Google、Microsoft、GitHub、Notion、Airtable），托管 OAuth |
| [n8n 工作流自动化](./skills/n8n-workflow-automation.md) 📖 | 88 | 🆓 | ✅ | 构建和触发 n8n 工作流 — 无代码自动化流水线 |
| [Mcporter](./skills/mcporter.md) 📖 | 114 | 🆓 | ✅ | MCP 服务器移植和管理 |
| [Nano Banana Pro](./skills/nano-banana-pro.md) 📖 | 206 | 🆓 | ✅ | 终端任务的瑞士军刀 — 高度定制化 |
| [OpenClaw 备份](./skills/openclaw-backup.md) 📖 | 43 | 🆓 | ✅ | 备份你的 OpenClaw 配置和工作区 |
| [模型使用统计](./skills/model-usage.md) 📖 | 88 | 🆓 | ✅ | 跨会话追踪 Token 使用量和模型成本 |
| [自动更新技能](./skills/auto-updater.md) 📖 | 280 | 🆓 | ✅ | 自动同步你已安装的技能到最新版本 |
| Clawdbot 文档专家 | 256 | 🆓 | ❌ | 从官方文档中回答 OpenClaw/Clawdbot 相关问题 |

---

## 🎨 创意与媒体

适合输出需要人类查看、收听或观看内容的场景。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| SuperDesign | 119 | 🆓 | ❌ | UI/UX 设计规范、组件描述、设计系统指导 |
| UI/UX Pro Max | 86 | 🆓 | ❌ | 高级设计评审、可访问性和原型规范 |
| [OpenAI 图片生成](./skills/openai-image-gen.md) 📖 | 24 | 🔑 | ✅ | 在聊天中通过 DALL-E 生成图片 |
| [Edge TTS 语音合成](./skills/edge-tts.md) 📖 | 22 | 🆓 | ✅ | 使用 Microsoft Edge 语音的文本转语音 — 免费、高质量 |
| [OpenAI Whisper 语音识别](./skills/openai-whisper.md) 📖 | 213 | 🔑 | ✅ | 使用 Whisper API 转录音频文件 |
| OpenAI Whisper API | 31 | 🔑 | ❌ | 轻量级 Whisper API 封装 |
| [YouTube 内容提取](./skills/youtube-watcher.md) 📖 | 217 | 🆓 | ✅ | 提取和总结 YouTube 内容 |
| 视频帧提取 | 79 | 🆓 | ❌ | 提取视频帧用于分析 |
| Gifgrep | 6 | 🆓 | ❌ | 搜索和下载 GIF — 轻量有趣的功能 |
| Spotify 播放器 | 35 | 🔑 | ❌ | 在聊天中控制 Spotify 播放 |
| Sonoscli | 40 | 🆓 | ❌ | 通过 CLI 控制 Sonos 音箱 |

---

## 💰 金融与市场

市场数据、投资组合监控和金融研究，请始终自行验证信息。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| 股票市场专业版 | 131 | 🆓* | ❌ | 全面的市场数据、筛选器和投资组合分析 |
| 股票监控 | 60 | 🆓 | ❌ | 监控股票价格并获取提醒 |
| [ByteRover](./skills/byterover.md) 📖 | 98 | 🆓 | ✅ | 金融数据聚合和分析 |

> ⚠️ **股票分析技能说明**（⭐161）：安全扫描标记 — 不包含在本列表中，建议使用股票市场专业版替代。
>
> *提供免费套餐；部分功能可能需要数据提供商密钥。

---

## 🏠 智能家居与系统

适合想要让 Agent 控制物理环境的用户。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [Home Assistant 集成](./skills/home-assistant.md) 📖 | 36 | 🔑 | ✅ | 完整的 Home Assistant 集成 — 设备、自动化、场景 |
| [天气查询](./skills/weather.md) 📖 | 294 | 🆓 | ✅ | 当前天气和预报 — 无需 API 密钥，全球可用 |
| [GoPlaces 位置服务](./skills/goplaces.md) 📖 | 26 | 🆓 | ✅ | 基于位置的地点搜索和导航 |
| [Apple 备忘录](./skills/apple-notes.md) 📖 | 40 | 🆓 | ✅ | 在 macOS 上读写 Apple 备忘录 |
| [1Password 集成](./skills/1password.md) 📖 | 34 | 🆓 | ✅ | 访问 1Password 保管库条目 — 只读，安全 |
| [Peekaboo 屏幕识别](./skills/peekaboo.md) 📖 | 51 | 🆓 | ✅ | macOS 视觉工具 — 识别屏幕上的内容 |
| [Gog 游戏库管理](./skills/gog.md) 📖 | 741 | 🆓 | ✅ | GOG 游戏启动器和库管理 |

---

## 🔒 安全

审计、加固和保护，不要跳过这部分。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [安全审计工具](./skills/security-auditor.md) 📖 | 19 | 🆓* | ✅ | 代码和配置的自动化安全评审 — 捕获常见漏洞 |
| [healthcheck 系统健康检查](./skills/healthcheck.md) 📖 ⚠️ | 8 | 🆓 | ✅ | 系统健康和安全加固 — 安装前请审核扫描结果 |
| 技能审核工具 | 427 | 🆓 | ❌ | 安装前审核任意技能 — 分析 SKILL.md 中的风险 |

> **专业建议：** 先安装技能审核工具，然后用它评估列表里的所有其他技能。

---

## ⚡ Agent 核心能力

这些技能会改变 Agent 的思考和行为方式，是所有其他功能的倍增器。

| 技能 | ⭐ | API 密钥 | 文档 | 描述 |
|-------|-----|---------|------|-------------|
| [自我提升 + 主动型 Agent](./skills/self-improving-agent.md) 📖 | 384 | 🆓 | ✅ | **这里最重要的技能。** Agent 永久向你学习，自我反思，持续提升 |
| [主动型 Agent](./skills/proactive-agent.md) 📖 | 557 | 🆓 | ✅ | Agent 无需询问就主动发起操作 — 监控和主动响应 |
| 主动型 Agent 轻量版 | 21 | 🆓 | ❌ | 更轻量的主动型 Agent 版本 — 资源占用更低 |
| [技能查找](./skills/find-skills.md) 📖 | 899 | 🆓 | ✅ | **ClawHub 上星标最多的技能。** 在 Agent 内部搜索和安装技能 |
| [内容总结](./skills/summarize.md) 📖 | 634 | 🆓 | ✅ | 核心工具 — 几乎在所有工作流中都会用到 |
| [自动更新技能](./skills/auto-updater.md) 📖 | 280 | 🆓 | ✅ | 自动保持所有技能为最新版本 |
| [Free Ride 智能路由](./skills/free-ride.md) 📖 | 274 | 🆓 | ✅ | 智能将任务路由到免费 AI 层级 — 降低成本 |
| [Gemini 模型集成](./skills/gemini.md) 📖 | 44 | 🔑 | ✅ | 添加 Google Gemini 作为模型选项 |
| 技能创建工具 | 150 | 🆓 ⚠️ | ❌ | 在 Agent 内部创建新技能 — 安装前先审核扫描结果 |
| [Evolver 自我进化](./skills/evolver.md) 📖 ⚠️ | 66 | 🆓 | ✅ | Agent 自我进化能力 — 实验性功能，使用前先审核扫描结果 |

> ⚠️ **Evolver 技能说明：** 多个版本都被安全扫描标记，视为实验性功能。

---

## 未收录的技能（及原因）

部分 ClawHub 上的技能被有意排除或标记为高风险：

| 技能 | 原因 |
|-------|--------|
| [Browser Use](./skills/browser-use.md) | 安全标记 — 可疑模式，已收录但标记为高风险 |
| [桌面控制](./skills/desktop-control.md) | 安全标记 — 已收录但标记为高风险 |
| 股票分析 | 安全标记 |
| Agent Browser (TheSethRose) | 安全标记 |
| 精英长期记忆 | 安全标记 |
| Playwright 爬虫技能 | 安全标记 |
| Web Search (billyutw) | 安全标记 |
| 重复条目 | Apple 提醒事项 ×4、Brave 搜索 ×2、Evolver ×3、百度搜索 ×2 — 已合并为单个条目 |

这并不意味着这些技能是恶意的 — ClawHub 安全扫描可能会产生误报，只是意味着你应该**在安装前审核扫描报告**。

---

## 贡献指南

发现值得收录的技能？欢迎提交 PR。

**添加技能的要求：**
1. 必须在 ClawHub 上发布，并且有可用的安装链接
2. 必须解决真实的工作流问题（不只是演示项目）
3. 必须通过"我会每周使用吗？"测试
4. 有安全标记的技能需要明确说明风险
5. 必须在 `./skills/` 目录下按照现有模板提供完整文档

**README 更新的 PR 格式：**
```markdown
| [技能名称](./skills/skill-name.md) 📖 | ⭐ 星标数 | 🆓/🔑 | ✅ | 一行描述 |
```

---

## 许可证

CC0 — 公共领域，自由使用。

---

*最后更新：2026年3月 | 技能来源：[ClawHub](https://clawhub.com) | 运行时：[OpenClaw](https://openclaw.ai)*
