---
title: "Apify"
type: entity
aliases:
  - "apify"
  - "Apify MCP"
  - "Apify Actors"
tags:
  - entity
  - 工具
  - 数据抓取
  - MCP
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Apify

## 摘要

**Apify** 是一个**网页抓取与数据提取平台**，拥有 **5,000+ 现成 Actors（爬虫）**，并官方提供 **MCP server**（`apify/apify-mcp-server`，MIT，7,185★）让 AI 助手直接调用。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它承担 Pipeline 一的数据采集：通过 Apify MCP 抓取 Reddit、Facebook 群组、YouTube 评论、TikTok 评论等平台近三个月的帖子与评论，构建买家画像。

> ✅ **已核实（2026-09-15 网络检索 + GitHub API）**：平台存在、MCP 接入方式、各平台 scraper 均与来源文章描述吻合。官方 MCP 仓库：https://github.com/apify/apify-mcp-server

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **形态** | 云端网页抓取与数据提取平台，以 "Actors" 为单位提供现成爬虫 |
| **Actor 数量** | 5,000+ 预构建 Actors（覆盖社交、电商、地图、搜索等） |
| **官方 MCP** | https://github.com/apify/apify-mcp-server （**MIT**，**7,185★**，2026-09-14 仍在推送） |
| **兼容客户端** | Claude、ChatGPT、Cursor、n8n 等所有 MCP 兼容客户端 |
| **计费** | **按计算单元（CU，$0.20/CU）** + Actor 用量；部分 Actor 按事件计费（pay-per-event） |
| **套餐（2026-09 核实）** | Free（**$5 平台额度/月，每月重置，无需信用卡**）／Starter $29/月（$26 年付）／Scale $199/月／Business $999/月／Enterprise 定制 |
| **代理费用** | 住宅代理 $8/GB；数据中心代理含免费额度后 $1/IP 起 |

### 来源中的用法

| 维度 | 描述 |
| --- | --- |
| **角色** | Pipeline 一（数字线索）的数据源：抓取买家聚集地的原话 |
| **接入方式** | Apify MCP——Agent 直接以 MCP 工具调用各平台的 scraper |
| **覆盖平台** | Reddit、Facebook 群组、YouTube 评论、TikTok 评论等（每个平台选合适的 scraper） |
| **数据要求** | 抓帖子和高赞评论、回复；保留每条的来源 URL、日期和互动量 |
| **时间窗口** | 最近三个月——"足够看出什么在重复，又不会旧到失效" |

### 各平台 scraper（"每个地方选合适的 scraper"的对应实现）

来源未指明具体 Actor。社区第三方实测整理的每平台默认选择（2026-05 快照，**非官方推荐**）：

| 平台 | 推荐 Actor | 用量/评分 | 价格 |
| --- | --- | --- | --- |
| Instagram | `apify/instagram-scraper` | 277K / 4.7★ | 从 $1.50 / 1K 结果 |
| TikTok | `clockworks/tiktok-scraper` | 185K / 4.7★ | $1.70 / 1K 结果 |
| YouTube | `streamers/youtube-scraper` | 82K / 4.8★ | $2.40 / 1K 视频 |
| Facebook | `apify/facebook-posts-scraper` | 74K / 4.5★ | $2.00 / 1K 帖子 |
| X / Twitter | `apidojo/tweet-scraper` | 57K / 3.9★ | 从 $0.40 / 1K 推文 |
| Reddit | `trudax/reddit-scraper` | 13K / 3.4★ | $45/月租用 + 用量（≈$4 / 1K 结果） |
| LinkedIn | `apimaestro/linkedin-profile-detail` | 11K / 4.5★ | $5.00 / 1K 资料 |

### 在本库中的角色

- 与本库熟悉的 MCP 生态呼应：Apify 以 **MCP server** 把大量现成 scraper 暴露给 Agent，是"Agent + 外部数据源"模式的典型样例。
- **成本口径提示**：官方按 CU / Actor 用量计费，"$5 免费额度"够小规模测试，但大规模抓取时**"按行计价"与"按可用数据行计价"会差量级**（例如 Twitter 原始行里可能有 90%+ 是转推/回复）；来源文章的"抓三个月数据"若照此执行需先测算成本。

### ⚠️ 合规边界（重要）

- Apify 官方与第三方文档均强调：**只抓公开可见（public-only）页面、不做登录绕过**。
- **LinkedIn 与 Facebook 的登录态数据是法律风险集中区**（合同条款与 CFAA 类主张），需**先取得书面许可**再跑。
- **个人数据处理一律触发 GDPR / CCPA**，与平台无关。
- 来源文章自带的合规声明提示"平台数据抓取在部分地区法规和平台规则下有限制，落地前请自行确认"——两处说法一致，本库保留该警示。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[grok-bot]]、[[hermes]]（调用方）、[[whop]]（Pipeline 一的下游投放）
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[GitHub apify/apify-mcp-server](https://github.com/apify/apify-mcp-server)（MIT，7,185★）、[Apify MCP 定价（toolradar 整理）](https://toolradar.com/tools/apify-mcp/pricing)、[各平台最佳 scraper（use-apify.com 第三方整理）](https://use-apify.com/docs/best-apify-actors/best-social-media-scrapers)、[SocialPilot MCP 工具对比](https://www.socialpilot.co/best-social-media-mcp-tools)

### 待核实

- 各平台 Actor 的价格/评分/用量为**第三方整理的 2026-05 快照**，非官方推荐，随 Actor 更新而变化，规模化前需以 Actor 页面的 Pricing 标签为准。
- "抓三个月数据"的实际成本未测算（取决于平台、数据量、是否需住宅代理）。
- 来源文章未指明所用具体 Actor 名称。

### 保留分歧

- **Reddit 抓取的可用性**：来源文章将其列为常规数据源，但第三方整理显示 Reddit Actor 为本表评分最低（3.4★，抱怨多集中在租用模式），实际稳定性需自行验证。
