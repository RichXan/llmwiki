---
title: "Anthropic"
type: entity
aliases:
  - "Anthropic 公司"
tags:
  - entity
  - 公司
  - AI
sources:
  - "[[从intent到闭环-ai原生sdlc]]"
  - "[[agent工程解析-上下文管理]]"
created: 2026-09-12
updated: 2026-09-12
---

# 实体：Anthropic

## 摘要

**Anthropic** 是 Claude 系列模型的开发公司。在本库中，它主要作为两条线索的源头出现：一是发布了 AI 原生 SDLC 的官方手册（[[ai原生软件开发]]），二是 [[claude-code]] 这一 agentic 编码工具的提供方，其上下文管理机制是 [[agent工程]] 的主要分析对象。

## 核心内容

### 基本信息

- **角色**：AI 模型与工具公司，Claude 系列模型开发方。
- **相关团队**：Applied AI 团队（《The AI-Native SDLC playbook》作者 [[louis-claxton|Louis Claxton]] 所属团队）。

### 与本库相关的关键动作

- **2026-08-21**：在 claude.com 博客发布《The AI-Native SDLC playbook》（[[ai原生软件开发]]），把企业客户落地 Claude Code 的经验整理成六个阶段的 play。中文解读见 [[从intent到闭环-ai原生sdlc]]。
- **API 设计特征**：Anthropic API 用 Messages 列表组织对话（`role`/`content`），并规定**工具执行结果必须封装为 `role: "user"` 的消息**（与 OpenAI 独立的 `role: "tool"` 不同）。详见 [[agent-loop]]。
- **模型与窗口**：来源提到 Anthropic 与 OpenAI 相继把上下文窗口做到 1M（[[上下文窗口]] 相关讨论见 [[上下文管理]]）。

### 相关产品（本库已收录的相关条目）

| 产品 | 说明 | 本库页面 |
| --- | --- | --- |
| Claude Code | agentic 编码工具（CLI），两篇来源的核心载体 | [[claude-code]] |
| Claude Design | 从 intent 出原型，再导出到 Claude Code 构建 | 暂无独立页 |
| Claude Security | 定期代码库扫描，Enterprise 公测功能，按消耗计费 | 暂无独立页 |
| Claude Tag | Claude 以自己身份加入 Slack 事故频道值班 | 暂无独立页 |
| Cowork | 非工程师使用 Claude 的入口之一 | 暂无独立页 |
| claude.ai | 网页端入口 | 暂无独立页 |

## 相关页面

- 实体：[[claude-code]]、[[openai]]、[[louis-claxton]]
- 概念：[[ai原生sdlc]]、[[意图文件]]、[[审批门]]、[[上下文管理]]
- 主题：[[ai原生软件开发]]、[[agent工程]]
- 来源：[[从intent到闭环-ai原生sdlc]]、[[agent工程解析-上下文管理]]

## 来源与待核实问题

- **来源**：[[从intent到闭环-ai原生sdlc]]、[[agent工程解析-上下文管理]]
- **待核实**：
  - Claude Security、Claude Tag、Cowork 的正式发布状态、定价与可用范围（来源中称仍在公测且限 Enterprise）。
  - 本页未做网络检索，产品清单以两篇来源的陈述为准。
