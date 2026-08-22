---
title: "用 Codex + Obsidian 搭建自生长的个人知识库实战"
type: source
aliases:
  - "自生长个人知识库实战"
  - "Codex Obsidian 知识库搭建"
tags:
  - source
  - article
  - 知识管理
  - LLM-Wiki
sources:
  - "[[raw/articles/用 Codex + Obsidian 搭建自生长的个人知识库实战]]"
created: 2026-08-17
updated: 2026-08-17
---

# 来源摘要：用 Codex + Obsidian 搭建自生长的个人知识库实战

## 摘要

本文作者 [[canghe|苍何]] 基于 [[karpathy|Karpathy]] 公开的 LLM Wiki 知识库构建方法与架构，实践了一套「自生长的个人知识库」。核心思路：用 [[workbuddy|WorkBuddy]] / [[codex|Codex]] 作为 Agent 执行层，用 [[obsidian|Obsidian]] 作为存储与呈现底座，把剪藏的文章、AI 对话、灵感持续沉淀为可进化的知识大脑。

文章拆解了 LLM Wiki 的核心理念（增量维护 vs 一次性 RAG 召回）、为什么选 Obsidian、Agent 能做什么，并给出三种从难到易的搭建方法：直接搭建法、claude-obsidian 插件、WeSight 知识大脑。

## 元信息

- **作者**：苍何（X：[@canghe](https://x.com/canghe)）
- **发布日期**：2026-08-09
- **原始链接**：https://x.com/canghe/status/2086372334089462208
- **原始文件**：`[[raw/articles/用 Codex + Obsidian 搭建自生长的个人知识库实战]]`
- **入库日期**：2026-08-17

## 核心内容

1. **LLM Wiki 的出发点**：主流 RAG / NotebookLM / 文件上传都是「临时召回+临时综合」，知识不累积；LLM Wiki 则给 AI 安排一份「长期维护知识库」的工作，每次增量处理都留下结构化结果。

2. **LLM Wiki 三层架构**：Raw 保存证据（只读）、Wiki 记录理解（Agent 全权维护）、Schema 定规则（AGENTS.md）。详见 [[llm-wiki-三层架构]]。

3. **为什么是 Obsidian**：本地化、数据自主、Markdown 纯文本、适合 Agent 读写、双链与图谱、插件生态；同时承担「存储底座、人机界面、知识观察窗口」三种角色。

4. **Agent（WorkBuddy / Codex）职责**：读取 Vault、识别概念/实体/主题、对照现有 Wiki、增量更新、建立双链、保留分歧、维护索引与日志。

5. **三种搭建方法**（按上手难度）：
   - 方法一「直接搭建法」：靠提示词 + AGENTS.md 手工搭，最灵活但门槛高。
   - 方法二「claude-obsidian 插件」：开源项目封装了 ingest / retrieve 等 Skill，降低门槛，但操作仍在 WorkBuddy / Codex 中。
   - 方法三「WeSight 知识大脑」：把入库、更新、检索整合进 Obsidian 内部，人机协作闭环最顺滑（当前仅会员内测）。

6. **模型选型**：长上下文 + 稳定的工具调用；文中点名 [[codex|Codex]] 内不建议用 GPT 5.6 Sol（用量过大），性价比可选 DeepSeek V4 Flash（不支持多模态），国内可选 Kimi K3、Doubao-Seed-Evolving。

## 相关页面

- 概念：[[llm-wiki]]、[[llm-wiki-三层架构]]
- 实体：[[obsidian]]、[[workbuddy]]、[[codex]]、[[wesight]]、[[claude-obsidian]]、[[karpathy]]、[[canghe]]
- 主题：[[自生长个人知识库]]

## 待核实问题

- ✅ 已核实（网络检索）：[[wesight|WeSight]] 与 [[claude-obsidian]] 均已定位到 GitHub 仓库（`freestylefly/wesight-obsidian`、`AgriciDaniel/claude-obsidian`），详见各自实体页。
- ⏳ 文中「WeSight 知识大脑」为会员内测功能，可用范围与正式发布时间**待核实**。
- ⏳ 文中提及的模型版本（DeepSeek V4 Flash、Kimi K3、Doubao-Seed-Evolving、GPT 5.6 Sol 等）具体能力与价格**待核实**。
- ⏳ 文末提到的「蓝皮书」「开源教程」具体地址未在正文给出，**待核实**。
- ⏳ 作者署名「苍何 / 苍河」写法差异需人工确认（见 [[canghe]]）。
