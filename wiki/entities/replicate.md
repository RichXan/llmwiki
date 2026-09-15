---
title: "Replicate"
type: entity
aliases:
  - "replicate"
  - "Replicate API"
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

# 实体：Replicate

## 摘要

**Replicate** 是一个**开源 AI 模型的托管/推理 API 平台**（2020 年成立，开创"AI 模型的 API"模式）：开发者可以用统一 API 运行数百个模型，也可**自托管自定义模型**。在 [[agent自动化获客完整指南|Chris Everest 获客指南]]中，它与 [[fal]] 并列作为**素材生成**的可选项中之一——"agent 通过 replicate 或 fal 来生成，看你给了它哪个的 key"。

> ✅ **已核实（2026-09-15 网络检索）**：平台存在，形态与来源描述吻合（按 API key 调用生成图像/视频素材）。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **定位** | 开源模型托管与推理 API 平台，兼社区模型市场 |
| **成立** | 2020 年 |
| **模型数量** | ~200 个（第三方 2026 对比口径）；社区可上传任意模型 |
| **特色** | **支持自定义模型托管（deploy your own）**、文档优秀、社区大 |
| **计费** | **按计算时长（per-second GPU time）**：GPU $0.0002–0.0012/秒（随 GPU 类型），另计冷启动/模型加载费用 |
| **免费额度** | $5（永久） |

### 与 fal 的对比（第三方整理，2026 快照）

| 维度 | Replicate | [[fal]] |
| --- | --- | --- |
| 模型数量 | ~200 | 985 endpoints（更多） |
| 价格 | 比 fal 贵 **30–50%** | 更低（多数场景最便宜） |
| 文档 / 社区 | **更好、更大** | 文档待完善、社区较小 |
| 自定义模型托管 | ✅ 支持 | ❌ 不支持 |
| 计费方式 | 按计算秒数（成本随模型效率波动） | 按输出计价（可预测） |
| 免费额度 | $5 | $10 |

典型图像价格对比（第三方口径）：Flux 2 Pro $0.055/张（fal $0.05）；Flux 2 Dev $0.03/张（fal $0.025）；SDXL $0.005/张（fal $0.003）。视频方面 fal 优势更明显（Wan 2.6：fal $0.05/秒 vs Replicate $0.09–0.25/秒）。

### 在本库中的角色

- 代表"**素材生成 API 聚合平台**"这一环节：来源文章把模型选择权交给执行时的 key 配置，agent 拿到哪个平台的 key 就用哪个。
- 与 [[apify]] 同属"Agent 的外部能力供给方"，但前者供数据、这里供内容生成。

## 相关页面

- 概念：[[skill文件]]
- 实体：[[fal]]（对照）、[[apify]]、[[grok-bot]]、[[hermes]]
- 主题：[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[agent自动化获客完整指南]]
  - 网络核实（2026-09-15）：[FAL.AI vs Replicate 对比（teamday.ai）](https://teamday.ai/blog/fal-ai-vs-replicate-comparison)、[2026 AI 图像视频 API 定价对比](https://www.teamday.ai/blog/ai-image-video-api-providers-comparison-2026)、[Replicate 定价指南（tokenmix）](https://tokenmix.ai/blog/replicate-pricing-guide)、[fal.ai vs Replicate（GMI Cloud）](https://www.gmicloud.ai/en/blog/fal-ai-vs-replicate)

### 待核实

- 模型数量（~200）、价格与对比数据为**第三方整理的 2026 快照**，非官方页面，且模型迭代快（如 Sora 2 API 已关停），需以官网为准。
- 来源文章未指明其场景中实际调用的模型。

### 保留分歧

- **成本优劣并非单向**：多数第三方向对比称 fal 更便宜，但 tokenmix 的测算指出 Replicate 在 **Flux Dev / SDXL 等"低硬件档"模型上可能更便宜**（因按实际计算秒数计费），而成因是 GPU 档位差异。两种说法**适用范围不同**，并列保留。
