---
title: "Grok Bot"
type: entity
aliases:
  - "grok bot"
  - "grok-bot"
  - "Grok 机器人"
tags:
  - entity
  - Agent
  - 产品
  - xAI
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Grok Bot

## 摘要

**Grok Bot** 是 xAI 于 **2026-08-11 发布（beta）** 的持久化 Agent 产品：每个 "Bot" 是一个**命名的 AI 队友**，运行在**自带一台持久云虚拟机**上（含浏览器、文件系统、终端），可以像人一样登录并操作你的工具，在你关闭笔记本后继续干活。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它是推荐的两种执行 Agent 之一（零配置、上手简单）。

> ✅ **已核实（2026-09-15 网络检索）**：产品存在、主体、形态均与来源文章描述吻合——"自带一台电脑，有终端、浏览器和文件系统，你像聊天一样跟它说话"。官方文档：docs.x.ai/grok-bot/overview。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **开发方** | xAI（新闻报道中亦称 "SpaceXAI"——xAI–SpaceX 合并后的公司；另有报道提及 SpaceX 于 2026-08-14 完成 对 Cursor 的收购，Cursor 与 xAI 共享账号计费体系） |
| **发布** | 2026-08-11（beta） |
| **官方文档** | http://docs.x.ai/grok-bot/overview ，下载页 x.ai/bot |
| **登录方式** | 需 **Cursor 或 SuperGrok 账号**认证 |
| **定价（2026-08/09 报道）** | Cursor Ultra $200/月；SuperGrok Heavy $300/月；Cursor Teams Premium $120/席/月；无免费档 |
| **平台** | macOS（Apple silicon / Intel）、Windows（x64 / Arm64）、iOS 18+（据 cual.ai：无 Linux / Android / iPad 版本；windowsmode 则称有 Linux 原生版——**两来源不一致，保留分歧**） |
| **许可** | 付费订阅制 |

### 核心机制

- **自有云电脑**：每个 Bot 跑在持久云 VM 上（浏览器 + 文件系统 + 终端），关机后任务继续；支持 connectors / MCP，无 API 的网站走 **computer use**（点击、输入、导航）。
- **像队友一样消息交互**：创建 Bot → 发消息交代任务 → 按需授权；无工作流构建器。
- **多 Bot 协作**：多个 Bot 并行运行，可互相发消息、在群聊中共享上下文、传递任务所有权。
- **Skills 与 Routines**：带 Bot 走一遍任务即可存为可复用 **skill**；包上 **routine**（定时如"工作日 8:00"或事件触发如 Slack 消息）后自动重跑，每 Bot 支持 50 个 routines。Teams 档含 **skills marketplace**。
- **Teach a task**：录屏演示最多 10 分钟工作流，Bot 从录像学习并转为 skill。
- **审批门**：发消息、发布内容、购买/转账、删除/覆写数据、改权限、生产变更等**默认需人工批准**；密码、2FA、支付确认由人接管虚拟机亲自输入。
- **安全注意**：同一账号下**所有 Bot 共享一台电脑**（文件、浏览器会话、登录态互通）；删除 Bot 不会清除共享文件与会话，需手动登出回收权限。

### 在本库中的角色

- [[agent自动化获客]] Pipeline 的零配置运行时：来源称"给 grok bot 一个 skill 文件和几个 key，它就开始干活"——与官方 skills 机制吻合（skill 可保存/导入；stremit.io 称入口在 Plugins → Installed → Private Plugins），但"直接投喂任意 .md 文件即运行"的具体导入方式**未在官方文档逐字核实**。
- 其 skills / routines / 审批门 与 [[skill文件]]、[[ai原生sdlc]] 的审批门思路同构，是"Agent 执行 + 人保留判断"分工的代表性产品实现。
- 与 [[claude-code|Claude Code]]（终端 Agent）、[[codex|Codex]] 构成对照：Grok Bot 走**云端常驻 VM** 路线，Claude Cowork 走本地桌面路线。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[hermes]]（指南中的另一执行 Agent，开源路线）、[[claude-code]]、[[codex]]
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[Grok Bot 官方文档](http://docs.x.ai/grok-bot/overview)、[cual.ai 报道](https://cual.ai/en/news/grok-bot-spacexai-agentes-con-computadora-propia)、[mem0.ai 指南](https://mem0.ai/blog/grok-bot-guide)、[windowsmode 介绍](https://www.windowsmode.com/grok-bot-for-windows/amp)、[stremit.io 概念解读](https://stremit.io/post/grok-bot-25-concepts-explained)

### 待核实

- 公司主体表述分歧（"xAI" vs "SpaceXAI"）与 xAI–SpaceX 合并、Cursor 收购细节，以官方口径为准。
- 平台覆盖分歧（是否支持 Linux）。
- 定价与套餐为 2026-08/09 新闻口径，可能变动。
- 来源文章"投喂 skill 文件即跑"的具体操作路径未在官方文档核实。
