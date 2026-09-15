---
title: "Earendil"
type: entity
aliases:
  - "earendil"
  - "Earendil Inc."
  - "Earendil Works"
tags:
  - entity
  - 公司
  - 开源
  - Agent
sources:
  - "[[armin-ronacher-九条反直觉判断]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Earendil

## 摘要

**Earendil Inc.** 是一家 **public benefit corporation（公益公司）**，2025 年由 [[armin-ronacher|Armin Ronacher]]（Flask / Jinja 作者）与 **Colin Daymond Hanna** 共同创立，定位是"开发**开放的、以人为导向**（human-directed）的 AI 软件"。2026 年 4 月收购开源 coding agent **[[pi-agent|Pi]]** 项目，并推出 **Lefos**（通过邮件提供 AI 协助）。

> ✅ **已核实（2026-09-15 网络检索）**：公司性质、创立者、收购 Pi 均获多方印证。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **全称** | Earendil Inc.（亦见 "Earendil Works" 表述） |
| **公司性质** | **public benefit corporation**（公益公司，非纯营利导向） |
| **创立** | 2025 年 |
| **创立者** | [[armin-ronacher|Armin Ronacher]]、**Colin Daymond Hanna** |
| **核心项目** | [[pi-agent|Pi]]（2026-04 收购，Earendil 持有项目所有权）、**Lefos**（通过邮件提供 AI 协助的产品） |
| **披露的早期支持者** | Accel（Daniel Levine）、Balderton（Daniel Waterhouse），以及 n8n 创始人 Jan Oberhauser、OpenClaw 创始人 Peter Steinberger、Revolut 的 Vlad Yatsenko、Sentry 的 David Cramer、Slack 的 Cal Henderson |

### 工程实践（据 AI Engineer 会议档）

Earendil 内部的共享工程实践，正是 [[armin-ronacher]] "面向 agent 可读的代码库"主张的落地：

- 显式组件边界；
- 集中式 SQL 访问；
- 可复用接口原语；
- **独特的函数名**（便于 agent 精确定位）；
- 禁止隐藏失败的 lint 规则。

### 与来源文章的呼应

- 来源文章第 07 条：Ronacher 自嘲 **Earendil 可能是唯一没有「自动修 issue 机器人」的 harness 公司**——「不是没试过软件工厂，是没成功」。
  - 该说法与 Earendil 的**"有意保留工程摩擦、人类理解优先于自主惯性"**立场一致（见 [[armin-ronacher]]），但"唯一"为自嘲式表述，**未核实**。
- 其"公益公司 + 开源 + 人为导向"的定位，与本库 [[自生长个人知识库]] 关注的开源知识资产治理、[[ai创业与需求发现]] 讨论的变现路径形成对照（**非营利导向 ≠ 无商业模型**，Lefos 即其商业化尝试）。

## 相关页面

- 概念：[[harness-极简主义]]、[[可内省性]]
- 实体：[[armin-ronacher]]、[[pi-agent]]、[[anthropic]]
- 主题：[[agent工程]]、[[ai原生软件开发]]
- 来源：[[armin-ronacher-九条反直觉判断]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[armin-ronacher-九条反直觉判断]]
  - 网络核实（2026-09-15）：[AI Engineer 演讲者档](https://ai.engineer/speakers/armin-ronacher)、[Pi (agent framework) Wiki](https://aiwiki.ai/wiki/pi_agent)、[Pi 工作流报道（runtimewire）](https://runtimewire.com/article/david-ondrej-armin-ronacher-pi-agent-workflow)

### 待核实

- 融资规模、估值、员工数等均未见披露。
- **Lefos** 的具体形态与商业模式（"通过邮件提供 AI 协助"）信息有限，未建独立页面。
- 名称拼写存在 "Earendil Inc." / "Earendil Works" 两种表述，规范名**待核实**。
- 收购 Pi 的日期有 2026-04-08 与 2026-05 两种说法（并列保留于 [[pi-agent]]）。
