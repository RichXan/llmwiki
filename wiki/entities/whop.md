---
title: "Whop（含 Whop Ads）"
type: entity
aliases:
  - "whop"
  - "whop ads"
  - "Whop Ads"
tags:
  - entity
  - 平台
  - 广告投放
  - 电商
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Whop（含 Whop Ads）

## 摘要

**Whop** 是一个数字产品/会员制内容交易平台（官方定位为金融科技公司，目标是"可持续收入生态"）。其广告产品 **Whop Ads**（**2026-05-12 上线**）让卖家**从 Whop 后台直接投放 Meta 广告（Facebook + Instagram）**，无需自建 Meta 广告账户。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]的 Pipeline 一中，Whop 承担**销售页托管、支付归因与广告投放**三个环节。

> ✅ **已核实（2026-09-15 网络检索）**：官方文档 https://docs.whop.com/manage-your-business/growth-marketing/ads 完整描述了来源文章提到的各项机制，**作者说法与官方文档高度一致**（详见下表）。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **定位** | 数字产品 / 会员制内容交易平台（官方自称金融科技公司） |
| **规模（官方口径）** | 40,000+ 月度创作者收入者；累计 2,200 万+ 买家；覆盖 145 国，年收入约 $40 亿 |
| **Whop Ads 上线** | 2026-05-12（Meta 集成） |
| **Whop Ads 负责人** | Nicholas Motamedi（Head of Whop Ads，Hidden Studios 创始人，该公司被 Whop 收购） |
| **CEO** | Steven Schwartz（联合创始人兼 CEO） |
| **官方文档** | https://docs.whop.com/manage-your-business/growth-marketing/ads （商家侧）；https://docs.whop.com/developer/ads/overview （开发者 Ads API） |

### 来源说法 vs 官方文档（逐条核对）

| 来源文章说法 | 官方文档核实 | 结论 |
| --- | --- | --- |
| 跑在 whop 自己的 Meta 代理账号上 | ✅ 官方：agency ad accounts on Meta，账户等级为 **"Platinum-tier HIVA"（Meta 最高层级）** | **已证实** |
| 竞价里优先、规模化后千次展示成本更低 | ✅ 官方原话："priority bidding and lower cost per thousand impressions at scale" | **已证实**（与来源文章措辞几乎一致） |
| 被拒次数远少于新账号 | ✅ 官方原话："Fewer thanks to higher account standing"，并称有**直接 Meta 代表 + Whop 客户经理**支持 | **已证实** |
| pixel 内置于 whop 页面，用真实支付数据归因 | ✅ 官方：**Whop Pixel** 是第一方归因 pixel，"Whop owns the underlying payments stack, so the pixel attributes conversions from real payment data instead of browser signals" | **已证实** |
| 转化回传给 Meta 优化系统 | ✅ 官方：Whop 通过 **Conversions API** 把转化转发给 Meta | **已证实** |
| 投放资金当天可从待结算余额支出 | ✅ 官方：三种出资方式——信用卡（2.9% 手续费，保留卡权益）／**Whop Card**（免手续费，广告支出 **5% 返现**）／**Pending Whop balance**（用未结算收入当天投放，不必等 4–5 天） | **已证实** |
| 用 whop ads 本身免费，只付投放花费 | ✅ 官方："No setup fees, no monthly fees, no minimum spend… you only pay for ad spend" | **已证实** |
| 拒收带承诺的素材（不能编收入数字、假证言、结果暗示） | ✅ 官方"Not allowed"清单：**Fake or unverifiable income claims / Fake testimonials / Scam-style or deceptive offers**；且投前跑内置合规检查 | **已证实** |
| 一条被拒会拖累整个广告组 | ✅ 佐证：`delivery_status` 中 `all_ads_rejected` 表示"活动中每个广告都被拒"导致停投；广告组/广告各自有 `delivery_status` | **基本证实**（机制存在，程度为作者表述） |
| 素材为竖版视频与静图、Meta 三种尺寸比例 | ⚠️ 官方未在本次检索的页面中明确列出尺寸比例；Ads API 支持 AI 生成图像/视频或自带素材 | **部分未核实** |

### 其他已核实的机制

- **多平台扩展**：Meta（Facebook + Instagram）已上线；**TikTok、Google、Snapchat、X、Reddit 均标注 "Coming soon"**——来源文章只讲 Meta，与现状一致。
- **无投放上限**：官方称 agency 广告账号**无每日消费上限**（标准个人账号有硬性平台限额）。
- **接入流程**：Ads 标签页 → OAuth 连接 Facebook 主页与 Instagram → Whop 自动创建 pixel（并用既有 Whop 销售数据预填充）→ 自助设置 **5 分钟内**完成；**无申请、无等待名单**。
- **广告层级（开发者视角）**：ad campaign → ad group → ad；预算只存在于一层（默认 ad group，或设 `budget_optimization=ad_campaign` 时在 campaign）。
- **归因口径**：所有业绩数字按 **Whop Pixel 归因**而非广告网络口径；`result_event` 命名判定事件，`results` 为 pixel 归因计数，`cost_per_result` = 花费 / 该计数。
- **一个 Whop 商家一个广告账号**；无信用额度，需用卡 / Whop Card / 待结算余额出资。

### 在本库中的角色

- 代表"**数字产品销售 + 广告投放一体化**"的平台模式：把支付、归因、投放打包，降低个人卖家投放门槛。
- 其**真实支付数据归因**与"每单成本 vs 产品价格"的评估口径，是 [[agent自动化获客]] 主题中少数可直接量化、且已获官方文档背书的指标。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[grok-bot]]、[[hermes]]、[[apify]]（Pipeline 一的上游数据）
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[Whop Ads 官方文档（商家侧）](https://docs.whop.com/manage-your-business/growth-marketing/ads)、[Whop Ads 官方文档（开发者 API）](https://docs.whop.com/developer/ads/overview)、[Whop Ads × Meta 深度解读（whatpayment）](https://whatpayment.com/en/blog/whop-ads-meta-integration)、[Whop Ads 官方发布稿转载（cmofirst / third-news）](https://cmofirst.com/marketing/whop-announces-meta-integration-for-whop-ads-its-built-in-advertising-product/)

### 待核实

- **素材尺寸**：来源称"用 Meta 的三种尺寸比例"，官方本次检索页面未明确列出，需查 Whop Ads 素材规范文档。
- **Meta 转向 invoice-only 计费**：whatpayment 提到 Meta 正在对许多广告主改为仅发票计费、会移除信用卡返现路径，而 Whop 的结构（你付 Whop、不直接付 Meta）保留卡通道——该变化对长期可用性的影响需持续观察。
- **平台适用范围**：是否对中国大陆卖家开放、支持哪些支付方式（含 Whop 出款）未知，**对国内落地是硬约束**。

### 保留分歧

- **每日消费上限**：来源文章未提及；官方文档称 agency 账号"无消费上限"，但 whats payment 的解读提到"账号从 Day 1 上限开始、逐日提升（1–2 周内推到高日消费）"——**两者表述不一致**（可能是文档与实操阶段差异），并列保留待验证。
