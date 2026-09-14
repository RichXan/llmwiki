---
title: "ChatGPT"
type: entity
aliases:
  - "Chat GPT"
tags:
  - entity
  - 产品
  - AI写作
sources:
  - "[[写作指南-ai真实文风]]"
created: 2026-09-14
updated: 2026-09-14
---

# 实体：ChatGPT

## 摘要

**ChatGPT** 是 [[openai|OpenAI]] 的对话式 AI 产品。在本库中，它作为 [[个人写作风格库]] 方案的载体出现：其 **Writing Style（写作风格）** 功能可从作者授权的数据源中归纳个人文风，配合 **Projects（项目层）** 与 **连接器**，形成"写作—定稿—归档—再参考"的闭环（见 [[写作指南-ai真实文风]]）。

## 核心内容

### 基本信息

- **开发方**：[[openai|OpenAI]]
- **形态**：对话式 AI 产品（网页版 / 应用），本库中作为 [[codex|Codex]] 之外的另一 OpenAI 产品出现

### 与本库相关的功能（来自来源）

| 功能 | 说明 |
| --- | --- |
| **Writing Style（写作风格）** | 位于「设置 → 个性化」下；可连接 Gmail、Google Drive、Slack、SharePoint 等数据源，参考你过去的邮件、消息和文章，提取写作习惯（措辞、句式、结尾习惯、大小写习惯等）并持续更新 |
| **Projects（项目层）** | 可写入归档指令与写作指令模板，让"定稿即归档"成为固定动作 |
| **连接器（Google Drive 等）** | 可查看/搜索 Drive 文件、读取 Google Docs/Sheets/Slides，并在明确要求时创建、整理或修改内容 |

- **开启路径**：ChatGPT 网页版 → 设置 → 个性化 → writing style（写作风格）→ 开始设置 → 数据来源选择 Google Drive；再在 ChatGPT 中连接 Google Drive 插件。

### 在本库中的角色

- 与 [[claude-code]]、[[codex]] 等编码 Agent 不同，ChatGPT 在本库中主要作为**通用写作/助手入口**出现。
- 其 Writing Style 是"以真实样本驱动文风"的**平台原生实现**，与 Skill 形态的 [[writing-style-skill]] 形成对照（同源异流，见 [[个人写作风格库]]）。

## 相关页面

- 实体：[[openai]]、[[codex]]、[[writing-style-skill]]
- 概念：[[个人写作风格库]]、[[去ai味]]
- 主题：[[ai写作去味]]
- 来源：[[写作指南-ai真实文风]]

## 来源与待核实问题

- **来源**：[[写作指南-ai真实文风]]

### 待核实

- Writing Style / Projects / 连接器的**具体可用范围、地区限制与套餐要求**（原文未说明）。
- 本页未做网络检索，功能细节以 ChatGPT 官方说明为准。
