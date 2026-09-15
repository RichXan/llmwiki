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
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Hermes Agent（Nous Research）

## 摘要

**Hermes Agent** 是 **Nous Research** 开源的自进化 Agent（口号 "The agent that grows with you"，GitHub：`NousResearch/hermes-agent`，**MIT 协议，245k+ stars**，持续活跃维护）。它常驻服务器、通过消息渠道（Telegram / Discord / Slack / WhatsApp / Signal / Email 等）与人交互，具备持久记忆、自主创建 skill、**cron 计划任务**等能力。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它是推荐的两种执行 Agent 之一（更技术化，但为计划任务而建）。

> ✅ **已核实（2026-09-15 网络检索 + GitHub API）**：产品存在、主体、形态均与来源文章描述吻合——"按计划运行、部署到 Railway、用 @BotFather 的 Telegram bot token、之后 prompt 通过 Telegram 发送"。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **开发方** | Nous Research |
| **仓库** | https://github.com/NousResearch/hermes-agent （MIT License） |
| **仓库指标（2026-09-15 GitHub API）** | ⭐ **245,618** stars / 51,198 forks；创建于 2025-07-22；最近推送 2026-09-15（活跃维护中） |
| **交互渠道** | 统一 gateway 接入：Telegram、Discord、Slack、WhatsApp、Signal、Email、Mattermost、Matrix；无网页聊天 UI |
| **模型接入** | 200+ 模型：OpenAI / Anthropic / Gemini / OpenRouter / DeepSeek / DashScope / **GLM（Z.AI）/ Kimi / MiniMax** / HuggingFace 等 |
| **工具集成** | 搜索（Tavily、Parallel）、抓取（Firecrawl）、图像生成（FAL）、浏览器自动化（Browserbase）、GitHub、语音（Whisper/TTS）、MCP server |
| **部署** | 可一键部署到 Railway（官方及社区模板，如 railway.com/deploy/hermes-agent-nous-research），数据持久化于 volume（`/root/.hermes`） |

### 核心机制

- **学习循环**：agent 自己管理记忆、自主创建 skill、skill 自我改进；FTS5 会话检索 + LLM 摘要。
- **Skills**：以 `~/.hermes/skills/<分类>/<技能名>/SKILL.md` 的文件形式存放，完成任务后可主动询问"要不要存为 skill"；支持 `skill_manage(action='patch')` 增量更新——**与 Claude Code Agent Skills 的 SKILL.md 约定同构**（详见 [[skill文件]]）。
- **Cron 计划任务**：内置 cron 调度器，可跨平台定时执行任务、结果投递到 Telegram——正对应来源文章"hermes 就是为计划任务而建的"。
- **Telegram 接入路径**：@BotFather 创建 bot → 填入 `TELEGRAM_BOT_TOKEN` → 配置允许的用户 ID → 配对审批后即可用——与来源文章描述的配置流程一致。
- **审批机制**：危险命令显示确认按钮而非直接执行（与 Grok Bot 的审批门同构）。

### 命名消歧（已核实）

- **Hermes Agent ≠ Hermes 模型系列**：两者同为 Nous Research 出品，但一个是 Agent 产品（本页），一个是开源模型系列（如 hermes-4-405B / hermes-4-70B，在 Hermes Agent 中可作 fallback 模型）。
- 2026-09-15 检索确认：来源文章中的 "hermes" 即指本产品（部署 Railway + Telegram + 计划任务的特征完全匹配）。

### 在本库中的角色

- [[agent自动化获客]] Pipeline 的常驻/定时运行时，与 [[grok-bot|Grok Bot]]（闭源、托管、零配置）构成**开源自托管 vs 商业托管**的对照。
- 与本库"自生长"理念呼应的另一个样本：agent 自主创建并改进 skill，"grows with you"。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[grok-bot]]（对照）、[[claude-code]]（配置撰写的 AI）
- 主题：[[agent自动化获客]]、[[自生长个人知识库]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[GitHub NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)（GitHub API：245,618★ / MIT / pushed 2026-09-15）、[Railway 一键部署模板（官方仓库）](https://railway.com/deploy/hermes-agent-nous-research)、[Railway 带官方 Dashboard 模板](https://railway.com/deploy/hermes-agent-with-official-dashboard)、[部署实录（dev.to）](https://dev.to/tessak22/how-i-deployed-hermes-agent-on-railway-with-telegram-and-every-gotcha-i-hit-along-the-way-4hhk)

### 待核实

- 来源文章称"给 Claude 一段 prompt + hermes 文档 + bot token 即可完成部署"——现 Railway 模板已提供图形化 Setup 向导，两种路径并存，文章所述的 prompt 部署路径未逐一复现。
- star 数为 2026-09-15 快照，随时间变化。
