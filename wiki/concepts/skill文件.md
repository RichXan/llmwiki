---
title: "Skill 文件（Agent 可移植工作流文档）"
type: concept
aliases:
  - "Skill 文件"
  - "Agent Skill"
  - "可移植工作流文档"
tags:
  - concept
  - Agent
  - 自动化
  - Prompt工程
sources:
  - "[[agent自动化获客完整指南]]"
created: 2026-09-15
updated: 2026-09-15
---

# 概念：Skill 文件（Agent 可移植工作流文档）

## 摘要

**Skill 文件**是一份用 Markdown 写成的可移植工作流文档：它告诉一个 agent "怎么干一件活"——步骤是什么、按什么顺序、用哪些工具、要记录什么、需要哪些 API key 和权限。**写一次，任何读到它的 agent 都能跑这个活。** 它出自 [[agent自动化获客完整指南|Chris Everest 获客指南]]：作者主张"不要把流程绑死在某一个 agent 上"，而是用 Claude（或 Codex）把整套 pipeline 写成一个 skill 文件，再交给 [[grok-bot|grok bot]] 或 [[hermes]] 执行。

## 核心内容

### 定义与结构

Skill 文件本质上是一份文档，包含：

| 部分 | 内容 |
| --- | --- |
| **规则层**（最上面） | 全局纪律，如：一个行业或一个细分一张表，绝不跨表读；任何会接触真人或花钱的动作，先停下来问人；不确定的东西标成 review，不要猜 |
| **步骤层**（按顺序） | 每一步说明用什么工具、读什么、写什么、把什么交给下一步 |
| **依赖清单** | agent 跑起来需要的所有 API key 和工具权限，让人一次性给全 |

写作标准："写得让一个从没看过这篇文章的 agent，只看文件就能跑起来。"

### 制作方法（来源给出）

把 pipeline 的各段 prompt 粘给 Claude，让它生成完整的 skill 文件：

> 把这些变成一个用于 [pipeline 一/二/三] 的 skill 文件。
> - 把运行规则放在最上面……
> - 然后按顺序列步骤……
> - 列出所有 API key 和工具权限……
> - 告诉我这里面哪些地方说得不够清楚、会让 agent 去猜

关键一环：**让 AI 自查文档中"会让 agent 去猜"的模糊点**——这与本库 [[AGENTS]] 中"存疑即停、不臆测"的纪律同构。

### 为什么"可移植"重要

- 流程与执行器解耦：skill 文件是核心资产，agent（grok bot / hermes）只是可替换的运行时；
- 门槛极低：普通人不用配置环境，"只要给 grok bot 一个文件和几个 key，它就开始干活"；
- 对撰写者的一次性投入换取跨 agent、跨任务的复用。

### 与各生态 Skill 机制的关系（2026-09-15 网络检索核实）

- **Claude Code / Anthropic Agent Skills**：本库既有的 [[stop-slop]]、[[humanizer-zh]]、[[shuorenhua]]、[[writing-style-skill]] 等都是该生态的具体 skill（.md 文件 + 规则 + 步骤）。
- **[[grok-bot|Grok Bot]]**：原生支持 **skills**（带 Bot 演示一遍任务即存为可复用 skill，或从 marketplace / Private Plugins 安装），并可包上 **routines** 定时重跑——与"skill 文件 + 计划执行"的用法吻合。
- **[[hermes|Hermes Agent]]**（Nous Research）：skill 以 `~/.hermes/skills/<分类>/<技能名>/SKILL.md` 文件形式存放，**与 Claude Code 的 SKILL.md 约定同构**；完成任务后可主动提议"存为 skill"，并支持增量 patch。
- 结论：原文"写一次 skill 文件，任何读到它的 agent 都能跑"的**可移植性主张，在三大生态（Claude Code / Grok Bot / Hermes）中均有对应的 skill 机制支撑**；但各生态 skill 的具体格式（目录结构、加载方式、frontmatter 字段）存在差异，跨生态直接复用同一份文件的兼容性**仍待实测**。

## 相关页面

- 实体：[[claude-code]]（撰写工具）、[[codex]]（亦可撰写）、[[grok-bot]]、[[hermes]]（运行时）
- 主题：[[agent自动化获客]]
- 同类实体（Claude Code 生态的具体 Skill）：[[stop-slop]]、[[humanizer-zh]]、[[shuorenhua]]、[[writing-style-skill]]、[[nuwa-skill]]、[[agent-style]]、[[taste-skill]]
- 来源：[[agent自动化获客完整指南]]

## 来源与待核实问题

- **来源**：[[agent自动化获客完整指南]]

### 待核实

- 原文未给出 skill 文件的完整示例，仅有生成它的 prompt 模板。
- 跨生态（Claude Code / [[grok-bot|Grok Bot]] / [[hermes|Hermes]]）直接复用同一份 skill 文件的兼容性**待实测**（2026-09-15 已核实三大生态均有 skill 机制，但格式细节有差异）。
