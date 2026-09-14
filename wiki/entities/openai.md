---
title: "OpenAI"
type: entity
aliases:
  - "OpenAI 公司"
tags:
  - entity
  - 公司
  - AI
sources:
  - "[[agent工程解析-上下文管理]]"
created: 2026-09-12
updated: 2026-09-12
---

# 实体：OpenAI

## 摘要

**OpenAI** 是 GPT 系列模型与 [[codex|Codex]] 等工具的开发公司。在本库中，它主要作为 [[anthropic|Anthropic]] 的对照出现：一是**上下文窗口做到 1M** 的行业动向，二是其 API 与 Anthropic API 在**工具结果回传方式**上的设计差异。本页信息较少，主要作用是支撑对照与溯源。

## 核心内容

### 与本库相关的两点

- **上下文窗口**：OpenAI 与 Anthropic 相继把窗口做到 **1M**，引发"上下文管理是否已过时"的讨论（Anthropic 侧已核实为 Opus 4.6 / Sonnet 4.6，约 2026-03 GA；**OpenAI 侧具体型号本次未确认**）——该问题的回答见 [[上下文管理]]。
- **API 设计差异**：OpenAI 专门设计了独立的 `role: "tool"` 来承载工具执行结果；而 Anthropic 规定工具结果必须封装为 `role: "user"`。这一差异影响 Agent Loop 的实现。详见 [[agent-loop]]。
- **产品**：[[codex]]（编码 Agent）本库已单独建页。

## 相关页面

- 实体：[[anthropic]]、[[codex]]、[[claude-code]]
- 概念：[[上下文管理]]、[[agent-loop]]、[[上下文窗口]]
- 主题：[[agent工程]]
- 来源：[[agent工程解析-上下文管理]]

## 来源与待核实问题

- **来源**：[[agent工程解析-上下文管理]]
- **已核实（网络检索，2026-09-12）**：其 API 用独立 `role: "tool"` 承载工具结果，与 Anthropic 的 `role: "user"` 设计差异属实（详见 [[agent-loop]]）。
- **仍待核实**：OpenAI 侧 1M 上下文窗口对应的具体模型型号与发布时间（本次检索未明确），本页未逐条核对官方文档。
