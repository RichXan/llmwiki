---
title: "Claude Code"
type: entity
aliases:
  - "ClaudeCode"
  - "CC"
tags:
  - entity
  - 工具
  - AI编程
  - Agent
sources:
  - "[[从intent到闭环-ai原生sdlc]]"
  - "[[agent工程解析-上下文管理]]"
created: 2026-09-12
updated: 2026-09-12
---

# 实体：Claude Code

## 摘要

**Claude Code** 是 [[anthropic|Anthropic]] 推出的 agentic 编码工具，也是本库两条来源的共同核心载体：在 [[ai原生软件开发]] 中它是 AI 原生 SDLC 的执行者（plan mode、hook、Skill、并行会话等能力的提供方）；在 [[agent工程解析-上下文管理]] 中它是**上下文管理机制**的剖析样本。本库用户环境为 Claude Code（见 [[log]] 用户约定）。

## 核心内容

### 上下文组成（新建会话约 25K tokens）

来源给出的初始化构成：工具定义（~10K，27 个工具的 JSON Schema）、主指令（~5K）、auto memory（~3K）、环境信息（~0.5K）、Skills 列表（~1.5K）、全局 `CLAUDE.md`（~100）、项目 `CLAUDE.md`（~4K）、当前日期（~50）、本地命令记录（~300）。逻辑分三层：静态指令层 / 弱动态层 / 强动态层。详见 [[上下文管理]]。

### 规则文件（CLAUDE.md）的五类形态

托管策略级（公司管机器）、用户全局级（`~/.claude/CLAUDE.md`）、项目共享级（`./CLAUDE.md`）、项目本地私有级（`./CLAUDE.local.md`）、子目录级（Monorepo）。装配按"系统托管 → 用户家目录 → 项目根 → 工作子目录"拼接，**不做物理覆盖**。详见 [[上下文管理]]。

### 关键机制（来自上下文管理来源）

- **渐进式加载**：Skill 只先加载名字与元数据，需要时才抓取完整指令。
- **工具延迟加载**：冷门工具只登记名字，通过 `tool_search` 按需拉取 Schema。
- **多级上下文压缩**：由轻到重依次为 大工具输出落盘 → Snip → Micro compact → Context collapse → Full compact。**注意**：不同来源对层数/命名有分歧，详见 [[上下文压缩]] 第五节。
- **Agent Loop**：Messages 单向追加；工具结果封装为 `role: user` + `tool_result`。详见 [[agent-loop]]。
- **1M 上下文窗口**：Opus 4.6 / Sonnet 4.6 起支持（约 2026-03 GA）。见 [[上下文窗口]]。

### 在 AI 原生 SDLC 中的角色

- 每个阶段的产物（[[意图文件|intent.md]]、`spec.md`、`plan.md`、PR）由 Claude 生成或审阅；人集中在 [[审批门]]。
- 提供 plan mode / auto mode、hook、Skill、子代理、并行会话等原语。
- 定位原则：**Skill 是建议性控制**，hook 是确定性控制。详见 [[建议性控制与确定性控制]]。
- 度量与治理建立在既有系统上（git、PR、CI）。详见 [[产物链]]。

### 同类工具对照

- 本库另有 [[codex]]（OpenAI 的编码 Agent）、[[claude-obsidian]]（把 Claude Code 用于知识库的第三方项目）。
- 工具差异的一个例证：OpenAI 用独立的 `role: "tool"` 回传工具结果，Anthropic 用 `role: "user"`。详见 [[agent-loop]]。

## 相关页面

- 实体：[[anthropic]]、[[codex]]、[[claude-obsidian]]、[[openai]]
- 概念：[[上下文管理]]、[[上下文压缩]]、[[agent-loop]]、[[ai原生sdlc]]、[[建议性控制与确定性控制]]
- 主题：[[agent工程]]、[[ai原生软件开发]]
- 来源：[[agent工程解析-上下文管理]]、[[从intent到闭环-ai原生sdlc]]

## 来源与待核实问题

- **来源**：[[agent工程解析-上下文管理]]、[[从intent到闭环-ai原生sdlc]]

### 已核实（网络检索，2026-09-12）

- **1M 上下文窗口**：Opus 4.6 / Sonnet 4.6 支持，约 2026-03 起 GA。
- **多级压缩流水线确实存在**：多个独立来源共同确认 Claude Code 有由轻到重的压缩机制（Micro compact / Snip / Context Collapse / 全量摘要）。
- 官方原文《The AI-Native SDLC playbook》（claude.com/blog）确认 Claude Code 在 AI 原生 SDLC 中的核心地位。

### 分歧 / 仍需人工确认

- 上下文组成的具体数字（约 25K 初始）、各 Token 阈值随版本变化，快照不代表当前版本。
- 压缩机制的层级归属、命名与阈值**在不同来源间存在分歧**（详见 [[上下文压缩]] 第五节），官方未给出统一权威定义。
- 本页未逐条核对官方文档；如需精确实现细节，应以 Anthropic 官方文档与源码为准。
