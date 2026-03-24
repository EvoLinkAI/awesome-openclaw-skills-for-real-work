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
| [Brave 搜索](./skills/brave-search.md)