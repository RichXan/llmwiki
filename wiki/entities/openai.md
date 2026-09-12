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

- **上下文窗口**：来源提到 OpenAI 与 Anthropic 相继把上下文窗口做到 **1M**，引发"上下文管理是否已过时"的讨论——该问题的回答见 [[上下文管理]]。
- **API 设计差异**：OpenAI 专门设计了独立的 `role: "tool"` 来承载工具执行结果；而 Anthropic 规定工具结果必须封装为 `role: "user"`。这一差异影响 Agent Loop 的实现。详见 [[agent-loop]]。
- **产品**：[[codex]]（编码 Agent）本库已单独建页。

## 相关页面

- 实体：[[anthropic]]、[[codex]]、[[claude-code]]
- 概念：[[上下文管理]]、[[agent-loop]]、[[上下文窗口]]
- 主题：[[agent工程]]
- 来源：[[agent工程解析-上下文管理]]

## 来源与待核实问题

- **来源**：[[agent工程解析-上下文管理]]
- **待核实**：1M 上下文窗口对应的具体模型型号与发布时间（来源未指明），本页未做网络检索。
