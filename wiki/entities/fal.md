---
title: "fal（fal.ai）"
type: entity
aliases:
  - "fal"
  - "fal.ai"
  - "FAL"
tags:
  - entity
  - 平台
  - 模型托管
  - API
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：fal（fal.ai）

## 摘要

**fal.ai** 是一个**生成式媒体模型 API 平台**（2023 年成立），以**聚合大量模型 + 低成本 + 快速推理**为定位：提供 985 个 endpoints，覆盖图像（406）、视频（450）、音频（59）、3D（35）、语音（35）。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它与 [[replicate]] 并列作为**素材生成**的可选项——"agent 通过 replicate 或 fal 来生成，看你给了它哪个的 key"。

> ✅ **已核实（2026-09-15 网络检索）**：平台存在，形态与来源描述吻合。第三方口径称其在图像 API 市场占 **50% 份额**、视频 API 占 **44%**（出自 State of Generative Media 报告，转引）。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **定位** | 生成式媒体模型聚合 API 平台，强调推理速度与成本效率 |
| **成立** | 2023 年 |
| **规模** | **985 endpoints**：图像 406 / 视频 450 / 音频 59 / 3D 35 / 语音 35 |
| **优势** | 模型最全、价格通常低 30–50%、部分模型独家（如 Kling O1）、全球 CDN 推理快 |
| **劣势** | 文档不如 Replicate 完善、社区较小、**不支持自定义模型托管** |
| **计费** | 按输出计价（每张/每秒），无最低消费；高用量有自动折扣 |
| **免费额度** | $10 |

### 图像价格（第三方口径，2026）

| 模型 | fal | [[replicate]] |
| --- | --- | --- |
| Flux 2 Pro | $0.05/张 | $0.055/张 |
| Flux 2 Dev | $0.025/张 | $0.03/张 |
| Flux 2 Schnell | $0.003/张 | $0.003/张 |
| SDXL | $0.003/张 | $0.005/张 |
| Seedream 5.0 | $0.04/张 | — |

### 视频价格（第三方口径，2026）

| 模型 | fal | 备注 |
| --- | --- | --- |
| Wan 2.6 | $0.05/秒 | Replicate $0.09–0.25/秒 |
| LTX 2.0 | $0.04/秒 | |
| Kling 3.0 Pro | $0.09/秒 | |
| Seedance 2.0 Fast | $0.04/秒 | Pro ~$0.05/秒 |
| Veo 3.1 Lite (720p) | $0.05/秒 | |
| Veo 3.1 + 音频 | $0.20/秒 | |

### 与来源文章说法的一致性

来源文章称："agent 通过 replicate 或 fal 来生成" "目前 **gpt image 2.5 是最好的图像模型，seedance 2.5 是最好的视频模型**，所以它会调这两个"。

核实结果：
- **平台与调用方式**：✅ 与 fal 的实际形态一致（统一 API 调用聚合模型）。
- **模型名称**：⚠️ 第三方资料显示 **Seedance 2.0**（字节跳动，2026-02 发布，Fast/Pro 双档）在 fal / ByteDance ModelArk 上可用；来源所写的 "seedance 2.5" **未在本次检索的资料中出现**，可能是作者的版本表述误差、后续版本或时点差异，**待核实**。同理 "gpt image 2.5" 亦未见对应记录（检索到的为 GPT Image 1.5）。
- **"最好"的判断**：属作者个人观点；第三方资料显示视频领域由 Seedance 2.0、Kling 3.0、Veo 3.1 及阿里 Wan-next 等多强竞争，"最好"无统一口径。

### 在本库中的角色

- 代表"**素材生成 API 聚合平台**"这一环节，与 [[apify]]（供数据）构成 Agent 外部能力的两个方向。
- 其"聚合多模型 + 按需选型"的形态，与 [[skill文件]] 主张的"流程与执行器解耦"思路同构：模型也可替换。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[replicate]]（对照）、[[apify]]、[[grok-bot]]、[[hermes]]
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[FAL.AI vs Replicate（teamday.ai）](https://teamday.ai/blog/fal-ai-vs-replicate-comparison)、[AI 图像视频 API 对比 2026](https://www.teamday.ai/blog/ai-image-video-api-providers-comparison-2026)、[fal.ai vs Replicate（GMI Cloud）](https://www.gmicloud.ai/en/blog/fal-ai-vs-replicate)

### 待核实

- endpoint 数量、市场份额、价格均为**第三方整理**，非官方页面，且模型迭代极快（该领域 2026 Q1 已多次换榜），需以官网为准。
- **"gpt image 2.5" 与 "seedance 2.5" 两个模型名未获证实**：检索到的对应版本为 GPT Image 1.5 与 Seedance 2.0。可能是版本表述误差或尚未收录的新版本，**不排除作者笔误**。
- 来源文章未指明其在 fal 上实际调用的模型。

### 保留分歧

- **成本优劣**：多数第三方向对比称 fal 更便宜，但 tokenmix 的测算指出 [[replicate]] 在低硬件档模型（Flux Dev / SDXL）上可按计算秒数更省——适用范围不同，并列保留。
