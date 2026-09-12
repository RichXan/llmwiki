---
title: "Agent Loop"
type: concept
aliases:
  - "Agent 循环"
  - "工具调用循环"
tags:
  - concept
  - Agent工程
  - API
sources:
  - "[[agent工程解析-上下文管理]]"
created: 2026-09-12
updated: 2026-09-12
---

# 概念：Agent Loop

## 摘要

**Agent Loop** 指 Agent 在"用户输入 → 模型响应 → 工具调用 → 结果回传 → 再推理"之间循环往返回的一次次往返。它是上下文在会话中如何增长的直接原因。来源以 [[anthropic|Anthropic]] API 与 [[claude-code]] 为例，给出四个关键场景。来源见 [[agent工程解析-上下文管理]]。

## 核心内容

### 消息结构

Anthropic API 用 Messages 列表组织对话，每条消息含两个核心参数：`role`（`user` / `assistant`）与 `content`（纯文本字符串，或由多个 Content Block 组成的列表）。

### 四个场景

1. **用户输入并发送**：组装为 `role: "user"` 消息，追加到上下文末尾。
2. **直接作答**：响应 `stop_reason: "end_turn"`，`content` 含 `text` 块；客户端把响应作为 `role: "assistant"` 追加。
3. **发起工具调用**：`stop_reason: "tool_use"`，`content` 含 `tool_use` 块（`id` 唯一标识、`name` 工具名、`input` 参数对象，结构遵循预先定义的 JSON Schema）。
4. **回传工具结果**：本地 Runtime 执行后，结果封装为一条消息，`content` 放 `tool_result` 块（`tool_use_id` 必须与 `tool_use.id` 完全一致）。

### 一个反直觉的细节

> 不同于 OpenAI 专门设计独立的 `role: "tool"`，**Anthropic 规定工具执行结果必须封装为 `role: "user"` 的消息。**

原因：在 Anthropic 的设计里，除了模型自己吐出的内容是 `assistant`，外部环境注入的一切反馈（真人输入、终端输出、报错）在身份抽象上都算"外部输入"，即 `user`。详见 [[openai]] 的对照。

### 与上下文管理的关系

- 每一步往返都把新消息**单向追加到末尾**，这是保证 [[kv-cache|KV Cache]] 命中的纪律。
- 工具结果往往是上下文膨胀的主要来源（见 [[上下文管理]] 的"六大 Token 杀手"），也是 [[上下文压缩]] 中 Micro compact 的主要清理对象。
- Loop 会持续到任务闭环：信息齐全则进入场景 2 给出最终答复，否则继续触发场景 3。

## 相关页面

- 概念：[[上下文管理]]、[[上下文压缩]]、[[kv-cache]]、[[上下文窗口]]
- 主题：[[agent工程]]
- 实体：[[claude-code]]、[[anthropic]]、[[openai]]
- 来源：[[agent工程解析-上下文管理]]

## 来源与待核实问题

- **来源**：[[agent工程解析-上下文管理]]
- **待核实**：示例中的 `stop_reason` 取值、字段命名以 Anthropic 官方 API 文档为准（本库未直接引用官方文档）。
