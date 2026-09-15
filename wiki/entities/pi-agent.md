---
title: "Pi（极简 agent harness）"
type: entity
aliases:
  - "Pi"
  - "pi-agent"
  - "Pi Agent"
tags:
  - entity
  - Agent
  - 开源
  - 工具
sources:
  - "[[armin-ronacher-九条反直觉判断]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：Pi（极简 agent harness）

## 摘要

**Pi** 是一个开源 coding agent / agent harness（TypeScript，MIT），以**刻意极简**为核心：默认只给模型**四个工具（read / write / edit / bash）**，系统提示与工具定义合计**不到 1,000 tokens**，其余能力通过**自扩展机制**由 agent 自己编写追加。2025-08 由 **Mario Zechner**（libGDX 作者）发起，**2026-04 被 [[earendil|Earendil]] 收购**（Zechner 加入并成为股东），由 Zechner、[[armin-ronacher|Armin Ronacher]] 与 Colin 共同主导技术方向。仓库：`github.com/earendil-works/pi`，官网 pi.dev。

> ✅ **已核实（2026-09-15 网络检索）**：项目存在，极简设计（含"基本只给你一个 bash"的说法）、与 Earendil/Ronacher 的关系均获佐证。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **类型** | 开源 coding agent / agent harness |
| **原创作者** | **Mario Zechner**（libGDX 作者），2025-08 起（初名 `badlogic/pi-mono`） |
| **归属** | **[[earendil|Earendil]] Inc.**（2026-04-08 宣布收购） |
| **仓库 / 官网** | `github.com/earendil-works/pi`；pi.dev |
| **协议 / 技术栈** | MIT（核心）；TypeScript，跑在 Bun 上 |
| **规模（第三方口径）** | 约 **80,000+ stars**、**1.3M+ npm 周下载**（2026 年中的快照） |
| **最新版本（检索所见）** | v0.84.1（2026-08-07） |

### 设计取向：刻意极简

- **四个核心工具**：read、write、edit、bash。**没有**原生 MCP 支持、没有 sub-agents、没有 plan mode、没有权限弹窗、没有内置 to-do、没有后台 shell 执行——**全部可由扩展补上**。
- **系统提示 < 1,000 tokens**（对比：Claude Code / Cline / OpenCode 等 harness 的系统提示约 7,000–10,000 tokens）。
- **为什么**：Zechner 的动机是不满既有 harness "功能堆积、版本间悄悄改系统提示、背着你注入上下文"；他要的是**对进入模型上下文的内容有精确控制**、完全可观测、可自托管模型。
- **扩展方式**：写 TypeScript 扩展；可以**直接让 Pi 自己写**（"Build me a skill that runs my Jest tests…"），扩展即时生效、无需重启 session。

### 与来源文章观点的呼应

| 来源文章说法（第 01 条） | 事实核查 |
| --- | --- |
| "所有 harness 的竞争都在收敛到基础功" | ✅ 与 Pi 的设计取向一致，且被描述为其核心论点 |
| "Pi 基本上只给你一个 bash" | ✅ 基本准确：默认四工具（read/write/edit/bash），**bash 是唯一的通用执行工具**；另有来源称其"无原生 MCP、无子代理" |
| "工具看似繁多的 Codex，底层也在大量调用 bash" | ⚠️ 未单独核实（属作者观察） |

### 在本库中的角色

- 代表**极简 harness 路线**的最激进样本，与 [[claude-code|Claude Code]]（batteries-included：sub-agents / hooks / MCP / plan mode）形成**鲜明对立的设计哲学**。
- **安全提示（重要）**：Pi 官方文档说明 agent 以**启动它的用户权限运行、无内置沙箱**，建议在容器 / VM / micro-VM 中运行，尤其针对不可信仓库或无人值守场景。采用 Ronacher 的工作流需自行还原隔离、凭据控制与审查习惯。

## 相关页面

- 概念：[[harness-极简主义]]、[[可内省性]]、[[skill文件]]、[[上下文管理]]
- 实体：[[armin-ronacher]]、[[earendil]]、[[claude-code]]、[[codex]]
- 主题：[[agent工程]]、[[ai原生软件开发]]
- 来源：[[armin-ronacher-九条反直觉判断]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[armin-ronacher-九条反直觉判断]]
  - 网络核实（2026-09-15）：[Pi (agent framework) Wiki](https://aiwiki.ai/wiki/pi_agent)、[Pi 评测（andrew.ooo）](https://andrew.ooo/posts/pi-coding-agent-minimal-terminal-harness-review)、[Pi 工作流报道（runtimewire）](https://runtimewire.com/article/david-ondrej-armin-ronacher-pi-agent-workflow)、[Pi 自扩展机制解读（byteiota）](https://byteiota.com/?p=15637/)

### 待核实

- star 数与版本号来自第三方快照，**不同来源数字不一致**（80,000+ / 85,000 / 58,000），需以 GitHub 实时数据为准。
- 收购日期有"2026-04-08"与"2026-05"两种表述（wiki 条目 vs 评测文章），并列保留。
- "系统提示 < 1,000 tokens"为项目自述口径，未逐字验证。
- 来源文章未直接讨论 Pi，本页为其观点与产品事实的交汇整理。
