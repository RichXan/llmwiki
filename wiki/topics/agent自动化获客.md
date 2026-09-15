---
title: "Agent 自动化获客"
type: topic
aliases:
  - "Agent 获客"
  - "自动化线索生成"
  - "Lead Generation Automation"
tags:
  - topic
  - Agent
  - 获客
  - 自动化
  - 增长
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
---

# 主题：Agent 自动化获客

## 摘要

用 Agent 全自动生成销售线索的完整方法论，出自 [[chris-everest|Chris Everest]] 的指南（见 [[agent自动化获客完整指南]]）。核心原则一句话：**"找到已经在付钱的人，把他们的数据抓下来，做出能触达他们的东西，然后放到他们看得见的地方。"** 全部流程打包成一个 [[skill文件|Skill 文件]]，由 [[grok-bot|grok bot]]（零配置）或 [[hermes]]（常驻计划任务）执行，人工只保留三件事：渲染图检查、与老板的第一次对话、广告预算。

> ⚠️ **合规提示（来源自带声明）**：冷启动短信/邮件触达与平台数据抓取在部分地区法规和平台规则下有限制，落地前需自行确认。

## 核心内容

### 三条 Pipeline 总览

| Pipeline | 适用人群 | 流程 | 变现 |
| --- | --- | --- | --- |
| **一 · 数字线索** | 有（或想有）数字产品的人 | 产品 → 买家画像（[[apify|Apify]] 抓 3 个月原话）→ 创意计划（3 angle × 3 hook）→ [[whop|whop ads]] 投放 → 跟进 | 自己的产品销售 |
| **二 · 实体线索** | 本地生意主人 | 选行业（公开数据可见的问题）→ 单一判定条件筛候选物业 → 图像模型渲染修复效果 → 邮件/短信/明信片触达 → 专属页面接回应 | 给自己的生意导流 |
| **三 · 卖线索** | 没有产品也没有生意的人 | Pipeline 二产出的线索 → Google Places 找老板自营企业 → 带 3 个线索样本触达 → 看板交付 | 首月按条收费，次月按月托管（zip code 独家） |

### 通用机制

- **[[skill文件|Skill 文件]]是核心**：用 [[claude-code|Claude]] 写一次，任何 agent 都能跑；流程与执行器解耦。
| Agent 选择 | [[grok-bot|grok bot]]（自带电脑、像聊天一样、零配置）vs [[hermes]]（部署到 Railway、Telegram 交互、为计划任务而建）。**Hermes 的另一面见 [[hermes私人助理养成指南]]**：同样是"自己选模型、接进常用聊天工具、连同积累一起迁走"的长期搭档 |
- **运行纪律**：一细分一张表绝不跨表读；接触真人或花钱的动作先停下来问；不确定标 review 不猜。

### 工具栈

| 环节 | 工具 | 核实状态 |
| --- | --- | --- |
| 数据抓取 | [[apify|Apify]]（MCP 接入，5,000+ 现成 Actors） | ✅ 已核实（官方 MCP MIT，7,185★） |
| 素材生成 | replicate / fal（作者称 gpt image 2.5 图像、seedance 2.5 视频为当时最佳） | ⚠️ 未核实（个人判断） |
| 广告投放与销售页 | [[whop|Whop Ads]]（Meta 代理投放、真实支付归因） | ✅ 已核实（Platinum-tier HIVA、Whop Pixel） |
| Agent 运行时 | [[grok-bot|Grok Bot]]（托管）／[[hermes|Hermes Agent]]（自托管） | ✅ 已核实 |
| 部署与交互 | Railway（hermes 部署）、Telegram（@BotFather） | ✅ 已核实（Railway 有一键模板） |
| 企业名单 | Google Places（评论数 15–200、老板自营） | ⚠️ 未核实 |

### 人机分工

Agent：寻找、读取、画像、素材、物业扫描、渲染、建页面、外联批次、表格、每日报告。**人只做三件事**：① 渲染图发出前检查；② 与商家老板的第一次对话；③ 广告预算（agent 提建议，人拍板）。

### 已知的坑（来源总结）

1. **公开影像过期**：读到的可能是三年前的图，问题已被修好——新区域第一批先验证影像新旧；
2. **广告素材合规**：whop ads 拒收承诺性素材（收入数字、假证言、结果暗示），一条被拒拖累整个广告组；
3. **触达回复率**：老板通常不回第一条消息，至少跟进两次。

### 与其他主题的关系

| 关联主题 | 关系 |
| --- | --- |
| [[ai创业与需求发现]] | **上游方法论**：本主题"找到已经在付钱的人"是 [[需求三等级]] 第三级（正在花钱解决）的操作化——一个判断什么值得做，一个给出怎么做起来 |
| [[agent工程]] | 层次互补：agent工程关注**单个 Agent 会话的技术实现**（上下文、压缩、记忆），本主题是 Agent 在**商业获客场景的应用层**；两者经由 [[skill文件]]（可移植工作流）衔接 |
| [[ai原生软件开发]] | 均为"Agent 承担执行、人保留判断"的分工模式；那边是审批门，这边是三件人工事项 |

## 相关页面

- 概念：[[skill文件]]、[[需求三等级]]
- 实体：[[chris-everest]]、[[grok-bot]]、[[hermes]]、[[apify]]、[[whop]]、[[claude-code]]
- 主题：[[ai创业与需求发现]]、[[agent工程]]、[[ai原生软件开发]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：[[agent自动化获客完整指南]]（目前单一来源；作者称方法基于其实践，未附实测数据）

### 待核实

- ~~[[grok-bot]] 与 [[hermes]] 的产品指向~~ **已核实（2026-09-15）**：grok bot = xAI **Grok Bot**（2026-08-11 beta，持久云 VM Agent，Cursor/SuperGrok 账号，$200–300/月）；hermes = **Nous Research Hermes Agent**（开源 MIT，`NousResearch/hermes-agent`，245k★，Telegram + cron 计划任务 + Railway 一键部署）。
- ~~"whop ads 处于 Meta 最高层级、被拒更少"~~ **已核实（2026-09-15）**：[[whop]] 官方文档确认 **Platinum-tier HIVA**、"priority bidding and lower cost per thousand impressions at scale"、"Fewer [rejections]"——与作者说法几乎逐字一致。**工具栈合规要求**亦获证实：[[apify|Apify]] 官方要求 public-only、LinkedIn/Facebook 登录态数据需先取得许可。
- "明信片效果远好于邮件/短信"为作者个人测试，无对照数据（未核实）。
- "gpt image 2.5 / seedance 2.5 为最佳图像/视频模型"为 2026-09 时点作者判断（未核实）。
- **合规边界**：各平台对抓取与冷触达的规则、各地区法规（如短信/邮件营销许可）需逐项确认后方可落地。
- 未见任何第三方复现或实测记录。
