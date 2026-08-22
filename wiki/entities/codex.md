---
title: "Codex"
type: entity
aliases:
  - "codex"
  - "OpenAI Codex"
tags:
  - entity
  - 工具
  - AI-Agent
sources:
  - "[[codex-obsidian-自生长个人知识库]]"
created: 2026-08-17
updated: 2026-08-17
---

# Codex

## 摘要

Codex 是 [[自生长个人知识库]] 系统中的 **Agent 执行层**工具之一（可与 [[workbuddy|WorkBuddy]] 互换）。它读取 Obsidian Vault，按 `AGENTS.md` 规则完成知识库的增量维护。

## 核心内容

### 在系统中的职责

- 直接读取 Obsidian Vault 目录与 Markdown 文件，调用搜索/脚本/命令批量处理。
- 按 `AGENTS.md` 约定工作：识别概念/实体/主题、对照现有 Wiki、增量更新、建立双链、保留分歧、维护索引与日志。
- 检索相关页面、整理答案、追溯来源，并批量检查失效链接、缺失字段、长期未更新内容。

### 模型选型提示（来自原文）

- 不建议用 Codex 里的 GPT 5.6 Sol（文中称「用量真的太猛了」）。
- 追求性价比可选 DeepSeek V4 Flash（但不支持多模态）。
- 长链路、多轮任务需关注：上下文容量、工具调用稳定性、指令遵循、结构化输出能力。

### 官方入口

- 官网：https://codexguide.ai/ （文中提及）

## 相关页面

- 工具：[[workbuddy]]、[[claude-obsidian]]、[[wesight]]
- 概念：[[llm-wiki]]、[[llm-wiki-三层架构]]
- 主题：[[自生长个人知识库]]
- 来源：[[codex-obsidian-自生长个人知识库]]

## 来源与待核实问题

- 来源：[[codex-obsidian-自生长个人知识库]]
- 待核实：文中「GPT 5.6 Sol 用量过大」为作者主观经验，具体依据**待核实**。
