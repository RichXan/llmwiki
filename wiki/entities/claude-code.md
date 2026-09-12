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
- **五级上下文防御**：大工具输出落盘 → Snip compact → Micro compact → Context collapse → Full compact。详见 [[上下文压缩]]。
- **Agent Loop**：Messages 单向追加；工具结果封装为 `role: user` + `tool_result`。详见 [[agent-loop]]。

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
- **待核实**：
  - 上下文组成的具体数字、Token 阈值随版本变化，快照中的数字不代表当前版本。
  - 五级防御中 Snip compact 等机制官方未完整公开，部分为作者推测。
  - 本页未做网络检索，官方文档链接待补。
