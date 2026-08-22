---
title: "LLM Wiki 三层架构（Raw / Wiki / Schema）"
type: concept
aliases:
  - "三层架构"
  - "Raw Wiki Schema"
  - "LLM Wiki 三层结构"
  - "LLM Wiki 三层架构"
tags:
  - concept
  - 知识管理
  - 架构
sources:
  - "[[codex-obsidian-自生长个人知识库]]"
created: 2026-08-17
updated: 2026-08-17
---

# LLM Wiki 三层架构（Raw / Wiki / Schema）

## 摘要

LLM Wiki 的三层架构是 [[llm-wiki|LLM Wiki]] 的知识组织方式：Raw 层保存原始证据（只读），Wiki 层沉淀 AI 整理的理解（可维护），Schema 层规定 AI 如何归档、更新、引用和处理冲突。一句话概括：**Raw 保存证据，Wiki 记录理解，Schema 负责定规则。**

## 核心内容

### 三层职责

| 层 | 目录 | 职责 | 权限 |
| --- | --- | --- | --- |
| Raw | `raw/` | 保存文章、论文、书籍、对话、笔记、会议等原始资料 | 只读，AI 不许改 |
| Wiki | `wiki/` | 保存 AI 整理出的概念、实体、主题 | AI 全权维护 |
| Schema | `AGENTS.md` | 给 AI 的工作说明书，定义归档/更新/引用/冲突规则 | 人工审慎修改 |

### Raw 子目录

`articles`（剪藏文章/网页）、`papers`（论文/报告）、`books`（书籍/划线/笔记）、`chats`（有价值的 AI 对话）、`notes`（灵感碎片）、`meetings`（会议纪要转写）。

### Wiki 子目录

`sources`（来源摘要页：一份 raw 资料对应一页）、`concepts`（概念页：方法论/理论/模式）、`entities`（实体页：人物/公司/产品/工具）、`topics`（主题综述页：跨领域综合对比）。

## 相关页面

- 概念：[[llm-wiki]]
- 主题：[[自生长个人知识库]]
- 来源：[[codex-obsidian-自生长个人知识库]]

## 来源与待核实问题

- 来源：[[codex-obsidian-自生长个人知识库]]
- 待核实：无
