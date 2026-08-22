---
title: "WeSight"
type: entity
aliases:
  - "WeSight 知识大脑"
  - "WeSight for Obsidian"
  - "wesight"
tags:
  - entity
  - 工具
  - Obsidian插件
sources:
  - "[[codex-obsidian-自生长个人知识库]]"
  - "https://github.com/freestylefly/wesight-obsidian"
  - "https://www.yeyulingfeng.com/a/919619.html"
created: 2026-08-17
updated: 2026-08-17
---

# WeSight

## 摘要

WeSight（全称 WeSight for Obsidian）是一款由 [[canghe|苍何]] 开发的 [[obsidian|Obsidian]] 插件，GitHub 开源（[freestylefly/wesight-obsidian](https://github.com/freestylefly/wesight-obsidian)，AGPL-3.0 协议）。核心理念是「让 AI 停在你的知识库里」——在 Obsidian 内直接调用 Claude Code、Codex 等 Agent，完成对话、写作、发布、同步等全链路，避免在多个工具间搬运。

在 [[自生长个人知识库]] 文章中，它对应**方式三（最顺滑）**：把知识库初始化、资料入库、Wiki 更新和智能检索整合进 Obsidian 内部，形成人机协作闭环。

## 核心内容

### 五重能力

1. **AI 对话侧边栏**：在 Obsidian 侧边栏直接与 Claude Code、Codex 或 OpenCode 对话；支持 `@mention` 引用笔记文件、斜杠命令、模型切换，AI 可读取整个知识库上下文。
2. **行内编辑（Inline Edit）**：选中任意文字，AI 给出修改建议，确认后替换。
3. **一键互联网分享**：生成 `share.wesight.ai` 链接，支持 Markdown 表格/代码块/公式/图片，读者可评论，更新/关闭/恢复可控。
4. **公众号草稿直推**：配置公众号信息后，把笔记直接推送到微信公众号草稿箱；内置苍河风格主题与 [[gzh-design]] Skill 的多种 AI 排版主题。
5. **飞书文档同步**：通过 Lark CLI 将笔记同步为飞书云文档；Token 存于操作系统密钥库，不进笔记、不进日志。

### 知识大脑（方式三核心）

- 开启「知识大脑」后，自动为当前 Vault 配置好环境与三层结构。
- 一键把当前笔记加入对应 Wiki。
- Chat 选择「基于知识库」模式时，优先检索已沉淀的 Wiki 页面，沿双链定位概念/实体/原始来源，自动完成检索、引用与上下文装配。
- 可把与 Claude Code、Codex 的聊天记录一键保存进知识大脑，沉淀为长期知识资产。

### 安装与配置

- 安装：Obsidian 设置 → 第三方插件 → 社区插件市场 → 搜索「WeSight」。
- 配置：可选择 Codex 模型（自动检测本机是否安装 Codex，含 Skill）；也可配置第三方 API（如 Claude Code）。

### 收费

- 绝大部分功能免费（排版、Chat 对话、标题封面生成等）。
- 部分需要服务器成本的功能采用积分付费；文中提及月会员最高赠 100 积分、约 15.9 元。

## 相关页面

- 工具：[[obsidian]]、[[claude-obsidian]]、[[workbuddy]]、[[codex]]
- 人物：[[canghe]]
- 概念：[[llm-wiki]]、[[llm-wiki-三层架构]]
- 主题：[[自生长个人知识库]]
- 来源：[[codex-obsidian-自生长个人知识库]]

## 来源与待核实问题

- 来源：
  - [[codex-obsidian-自生长个人知识库]]（「知识大脑」三层架构用法）
  - https://github.com/freestylefly/wesight-obsidian （项目仓库与协议）
  - https://www.yeyulingfeng.com/a/919619.html （五重功能详述）
- 待核实：
  - 「知识大脑」当前是否仍为会员内测、正式开放时间**待核实**（原文称内测，后续评测文章已描述更多功能）。
  - 积分/会员定价的实时标准与历史版本差异**待核实**。
  - 作者署名存在「苍何 / 苍河」两种写法，需确认是否为同一人（见 [[canghe]]）。
