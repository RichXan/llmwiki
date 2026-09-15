---
title: "Apify"
type: entity
aliases:
  - "apify"
  - "Apify MCP"
tags:
  - entity
  - 工具
  - 数据抓取
  - MCP
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
---

# 实体：Apify

## 摘要

**Apify** 是一个**网页抓取/数据提取平台**，在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中承担数据采集环节：它对 Reddit、Facebook 群组、YouTube 评论、TikTok 评论等平台各自提供现成的 scraper（爬虫），Agent 通过 **Apify MCP** 调用，用于抓取目标社群近三个月的帖子与评论、构建买家画像。

## 核心内容

### 来源中的用法

| 维度 | 描述 |
| --- | --- |
| **角色** | Pipeline 一（数字线索）的数据源：抓取买家聚集地的原话 |
| **接入方式** | Apify MCP——Agent 直接以 MCP 工具调用各平台的 scraper |
| **覆盖平台** | Reddit、Facebook 群组、YouTube 评论、TikTok 评论等（每个平台选合适的 scraper） |
| **数据要求** | 抓帖子和高赞评论、回复；保留每条的来源 URL、日期和互动量 |
| **时间窗口** | 最近三个月——"足够看出什么在重复，又不会旧到失效" |

### 在本库中的角色

- 与本库熟悉的 MCP 生态呼应：Apify 以 **MCP server** 的形式把大量现成 scraper 暴露给 Agent，是"Agent + 外部数据源"模式的典型样例。
- 数据抓取的**合规性**是使用前提（见来源自带的合规声明：平台规则与地区法规可能限制抓取行为）。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[grok-bot]]、[[hermes]]（调用方）
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：[[agent自动化获客完整指南]]

### 待核实

- 本页信息来自单一来源文章，Apify 的官网、定价、MCP server 的官方接入文档未做网络核实。
- 各平台 scraper 的实际可用性与合规边界（尤其 Facebook / TikTok 对抓取的规则限制）。
