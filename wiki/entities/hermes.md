---
title: "Hermes Agent（Nous Research）"
type: entity
aliases:
  - "hermes"
  - "Hermes"
  - "hermes-agent"
tags:
  - entity
  - Agent
  - 工具
  - 开源
  - NousResearch
sources:
  - "[[agent自动化获客完整指南]]"
  - "[[hermes私人助理养成指南]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Hermes Agent（Nous Research）

## 摘要

**Hermes Agent** 是 **Nous Research** 开源的自进化 Agent（口号 "The agent that grows with you"，GitHub：`NousResearch/hermes-agent`，**MIT 协议，245k+ stars**，持续活跃维护）。它常驻服务器、通过消息渠道（Telegram / Discord / Slack / WhatsApp / Signal / Email 等）与人交互，具备持久记忆、自主创建 skill、**cron 计划任务**等能力。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它是推荐的两种执行 Agent 之一（更技术化，但为计划任务而建）；在 [[hermes私人助理养成指南]] 中，它是"**能看见、能修改、能带走**"的私人助理（**自己选模型、接进常用聊天工具、连同积累一起迁走**）。

> ✅ **已核实（2026-09-15 网络检索 + GitHub API）**：产品存在、主体、形态均与来源文章描述吻合——"按计划运行、部署到 Railway、用 @BotFather 的 Telegram bot token、之后 prompt 通过 Telegram 发送"。
>
> 📘 **官方文档站**：`https://hermes-agent.nousresearch.com/`（`/docs/getting-started`、`/docs/user-guide`、`/docs/user-guide/features`、`/docs/user-guide/messaging` 等路径）

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **开发方** | Nous Research |
| **仓库** | https://github.com/NousResearch/hermes-agent （MIT License） |
| **仓库指标（2026-09-15 GitHub API）** | ⭐ **245,618** stars / 51,198 forks；创建于 2025-07-22；最近推送 2026-09-15（活跃维护中） |
| **口号 / 定位** | "The agent that grows with you"；**能从做事过程中积累经验的长期助理** |
| **交互渠道** | 统一 gateway 接入：Telegram、Discord、Slack、WhatsApp、Signal、Email、Mattermost、Matrix、**微信（腾讯 iLink Bot 私聊）**；无网页聊天 UI |
| **模型接入** | 200+ 模型：OpenAI / Anthropic / Gemini / OpenRouter / DeepSeek / DashScope / **GLM（Z.AI）/ Kimi / MiniMax** / HuggingFace 等；**含 ChatGPT / Codex 订阅登录**与 **xAI API / xAI Grok OAuth**（可接 SuperGrok / Premium+ 订阅）两条复用已有账户的路线 |
| **工具集成** | 搜索（Tavily、Parallel）、抓取（**Firecrawl**）、图像生成（FAL）、浏览器自动化（Browserbase，亦支持 **Use My Real Browser Profile** 复用本机登录态）、GitHub、语音（Whisper/TTS）、MCP server |
| **部署** | 可一键部署到 Railway（官方及社区模板，如 railway.com/deploy/hermes-agent-nous-research），数据持久化于 volume（`/root/.hermes`）；也支持**本地网关 / 远程 SSH 网关**切换 |
| **安装** | 桌面安装器（Mac / Windows / Linux，**已不再支持 Intel Mac**）；脚本安装：Linux/WSL2 `curl -fsSL https://hermes-agent.nousresearch.com/install.sh \| bash`，Windows PowerShell `iex (irm https://hermes-agent.nousresearch.com/install.ps1)` |

### 核心机制

- **学习循环**：agent 自己管理记忆、自主创建 skill、skill 自我改进；FTS5 会话检索 + LLM 摘要。
- **Skills**：以 `~/.hermes/skills/<分类>/<技能名>/SKILL.md` 的文件形式存放，完成任务后可主动询问"要不要存为 skill"；支持 `skill_manage(action='patch')` 增量更新——**与 Claude Code Agent Skills 的 SKILL.md 约定同构**（详见 [[skill文件]]）。
- **Cron 计划任务**：内置 cron 调度器，可跨平台定时执行任务、结果投递到 Telegram——正对应来源文章"hermes 就是为计划任务而建的"。支持 **continuity（连续记住上次结果）** 过滤已汇报内容，也支持 `context_from` **链式任务**。
- **Telegram 接入路径**：@BotFather 创建 bot → 填入 `TELEGRAM_BOT_TOKEN` → 配置允许的用户 ID → 配对审批后即可用——与来源文章描述的配置流程一致。
- **审批机制**：危险命令显示确认按钮而非直接执行（与 Grok Bot 的审批门同构）。三档：Smart / Manual / Off。

### 私人助理用法要点（出自 [[hermes私人助理养成指南]]）

**命令与入口速查**（**均取自该文，本批未逐一打开官方文档核对**）：

| 命令 | 作用 |
| --- | --- |
| `hermes model` | 模型接入向导（**订阅登录走"账号"，不要误进"API 密钥"**，后者按 API 计费） |
| `hermes config path` | 返回 `config.yaml` 位置（**SOUL.md 就在其旁边**） |
| `hermes config set / get / unset` | 修改 / 查看 / 清除设置 |
| `hermes tools` | 工具与密钥配置 |
| `/learn` | 从资料（网页、文档目录、PDF）或刚完成的工作流学一项新技能 |
| `/journey` | 打开**学习记录星图**，查看积累了哪些内容，可直接编辑或删除 |
| `/review` | 派**独立审阅者**读文件、调工具检查刚才的成果 |
| `/refine` | 手动触发复盘（关闭自动复盘时用） |
| `/rollback`、`/rollback diff 编号`、`/rollback 编号 文件路径` | 文件检查点回退（**只能恢复本地文件**） |
| `/memory pending`、`/memory approve 编号`、`/memory reject 编号` | 消息入口下处理待批记忆 |
| `hermes profile export / import` | **角色导出/导入**（记忆、性格、Skill 和配置随角色迁移；知识库目录需另行同步） |
| `hermes -p <profile> cron create / list / run / pause / resume` | 按角色管理定时任务 |
| `hermes -p <profile> gateway setup / run` | 消息网关配置与前台运行 |
| `hermes -p <profile> pairing approve <platform> <码>` | 消息入口**配对审批** |
| `hermes skills install <SKILL.md URL>` | 从 URL 安装 Skill |

**关键配置推荐值**（该文作者给出）：

| 项 | 推荐值 | 备注 |
| --- | --- | --- |
| 代码执行模式 / 持久化 Shell / 环境变量透传 / 文件读取上限 | Project / 打开 / 留空 / 100000 | 文件读取上限是**单次读取字符数**，不是知识库容量 |
| **记忆预算 / 画像预算** | **2200 / 1375 字符** | 这些内容**随每次请求进入上下文**；预算不够时**先删过期内容**，别一开始扩成几万字 |
| 记忆写入审批 | `memory.write_approval` 个人专用先关 | ⚠️ **"开了审批却一直不处理，助理的记忆就会停在待确认状态"** |
| 后台复盘 | `auxiliary.background_review.enabled true` | ⚠️ **同主模型的后台复盘会继承主任务的推理强度**，想降用量须另选辅助模型 |
| **压缩阈值 / 保护最近消息 / 压缩目标** | **0.5 / 20 / 0.2** | ⚠️ **合同数字、引文和正式决定应落进文件，不能只依赖压缩摘要** |
| 审批档位 | **Smart，超时 300 秒，白名单留空** | ⚠️ "不要为了少点几次按钮，把宽泛命令加进白名单" |
| 文件检查点 | `checkpoints.enabled true` | 会反复改笔记/文档就开 |
| 时区 | `timezone Asia/Shanghai` | ⚠️ **装在海外服务器上时，不要依赖服务器本地时区** |
| 无人值守 | `approvals.cron_mode deny`、`approvals.unattended_mode deny` | 保留拒绝危险操作 |
| Warm Bot Backends | 2–3 个 | 每多保留一个后台约多占 60 MB 内存 |

**三层权限框架**（该文作者的总结，可复用）：① **审批**（能不能拦住）→ ② **文件检查点**（能不能回退）→ ③ **执行环境**（在哪儿跑：Local / Docker 隔离）。这三层与本库既有的 [[审批门]]、[[可内省性]] 概念互补——**审批门解决"拦住"，检查点解决"撤回"，可内省性解决"人是否理解发生了什么"**。

**定时任务的两个硬约束**（该文强调）：

1. **工作目录不能省略**——定时任务默认使用**网关启动时所在的目录**，不一定是你当前桌面会话的目录；
2. **它归属于创建它的网关**——**远端网关停机，桌面开着也不会替它执行**。

**"养成"的两个关键机制**：

- **角色（BOTS / profiles）分工**：可以建 `my-researcher`（研究员：查官方来源、保留链接）与 `my-checker`（核查员：打开原始来源、核对关键事实、只列影响结论的问题），**两者共用同一工作目录才能围绕同一份成果接力**。克隆 default 只为复用账户，**Skill 要做减法**。
- **后台复盘 + `/journey`**：agent 从你的纠正、成功步骤和踩过的坑里提取经验更新记忆或技能，而你能**看见、编辑、删除**它学到的东西——这正是本库"自生长"理念在 Agent 产品上的实现形态。

### 私人助理向 Skill（出自 [[hermes私人助理养成指南]]）

| Skill | 解决什么 | 来源 |
| --- | --- | --- |
| **OpenCLI**（`jackwener/OpenCLI`） | 让助理去**你已登录的网站**找真实反馈与原帖 | 第三方仓库 |
| **QMD** | **先翻旧资料再给新建议**（从文章/笔记/会议记录找回原文） | 官方 `optional-skills/research/qmd` |
| **Blogwatcher** | 保存**订阅与已读状态**，只报告新内容 | 官方 `optional-skills/research/blogwatcher` |
| **Email Inbox Triage** | 沿完整邮件线程找出**谁该行动、谁在等待**，先写回复草稿 | **官方内置** `skills/email/email-inbox-triage` |
| **Weekly Review Planning** | 找出**停滞项目、答应过却没做的事、正在等的回复** | **官方内置** `skills/productivity/weekly-review-planning` |

> ⚠️ 该文反复强调的配置纪律：**第一次都先小范围试**（小资料夹 / 两个订阅源 / 三到五条邮件线程），人工核对可靠后再扩大权限；**只读优先**；**看不清的金额留给用户确认，不要让它为了填满表格自动猜**。

### 与既有页面的分工

- **本页（实体页）**：收录"**是什么**"的产品事实与网络核实结论。
- **[[hermes私人助理养成指南]]（来源页）**：收录"**怎么用**"的实操细节（安装、设置、BOTS、微信接入、5 个 Skill、5 位海外玩家的生活用法）。
- 两者不重复；如需操作步骤请直接看来源页。

#### 本库既有的三个 Hermes 使用场景

| 场景 | 来源 | 角色 |
| --- | --- | --- |
| **获客 Pipeline 的定时执行器** | [[agent自动化获客完整指南]] | 按计划抓数据、发触达 |
| **私人助理（长期搭档）** | [[hermes私人助理养成指南]] | 收件箱/资料库/成果三层工作流、"记一下/找一下/整理一下"、周复盘 |
| **与 Grok Bot 的对照样本** | 同上 | **开源自托管 vs 商业托管**；"自由" vs "省心" |


### 命名消歧（已核实）

- **Hermes Agent ≠ Hermes 模型系列**：两者同为 Nous Research 出品，但一个是 Agent 产品（本页），一个是开源模型系列（如 hermes-4-405B / hermes-4-70B，在 Hermes Agent 中可作 fallback 模型）。
- 2026-09-15 检索确认：来源文章中的 "hermes" 即指本产品（部署 Railway + Telegram + 计划任务的特征完全匹配）。

### 在本库中的角色

- [[agent自动化获客]] Pipeline 的常驻/定时运行时，与 [[grok-bot|Grok Bot]]（闭源、托管、零配置）构成**开源自托管 vs 商业托管**的对照。
- 与本库"自生长"理念呼应的另一个样本：agent 自主创建并改进 skill，"grows with you"。

## 相关页面

- 概念：[[skill文件]]、[[长期记忆]]、[[上下文压缩]]、[[审批门]]
- 实体：[[grok-bot]]（对照）、[[claude-code]]（配置撰写的 AI）、[[obsidian]]（资料库场景）
- 主题：[[agent自动化获客]]、[[agent工程]]、[[自生长个人知识库]]
- 来源：[[agent自动化获客完整指南]]、[[hermes私人助理养成指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]、[[hermes私人助理养成指南]]
  - 网络核实（2026-09-15）：[GitHub NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)（GitHub API：245,618★ / MIT / pushed 2026-09-15）、[Railway 一键部署模板（官方仓库）](https://railway.com/deploy/hermes-agent-nous-research)、[Railway 带官方 Dashboard 模板](https://railway.com/deploy/hermes-agent-with-official-dashboard)、[部署实录（dev.to）](https://dev.to/tessak22/how-i-deployed-hermes-agent-on-railway-with-telegram-and-every-gotcha-i-hit-along-the-way-4hhk)

### 待核实

- 来源文章称"给 Claude 一段 prompt + hermes 文档 + bot token 即可完成部署"——现 Railway 模板已提供图形化 Setup 向导，两种路径并存，文章所述的 prompt 部署路径未逐一复现。
- star 数为 2026-09-15 快照，随时间变化。
- **本批新增的"私人助理用法要点"全部出自 [[hermes私人助理养成指南]]，未逐一打开官方文档核对**，包括：`/learn`、`/journey`、`/review`、`/refine`、`/rollback`、`/memory pending`、`profile export/import`、`cron ... --continuity`、`gateway setup`、`pairing approve` 等命令与参数；以及记忆预算 2200/1375 字符、压缩阈值 0.5、保护最近消息 20、审批超时 300 秒等推荐值（**这些是作者推荐值，不一定等于官方默认值**）。
- **官方文档站 `hermes-agent.nousresearch.com` 未直接打开核实**；文中引用的文档 tag **`v2026.9.7`** 未核实是否存在。
- **"当前官方支持表不再支持 Intel Mac"**为来源对该文官方平台支持表的转述，未直接核对。
- **微信（腾讯 iLink Bot）** 的适用范围、是否对中国大陆以外地区开放、普通微信群不投递的边界**未核实**。
- **`xAI Grok OAuth` 接 SuperGrok / Premium+ 订阅**的可用性未核实。

