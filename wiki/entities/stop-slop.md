---
title: "stop-slop"
type: entity
aliases:
  - "stop-slop-zh"
  - "stop slop"
tags:
  - entity
  - 工具
  - Skill
  - 去AI味
sources:
  - "[[去ai味完整实战教程]]"
  - "https://github.com/hardikpandya/stop-slop"
created: 2026-08-17
updated: 2026-08-17
---

# stop-slop

## 摘要

stop-slop 是「把 AI 最爱用的写作套路整理成检查规则，然后逐条清理」的去 [[去ai味|AI 味]] Skill。它的问法不是"这是不是 AI 写的"，而是"这段文字里有没有 AI 最容易产生的坏习惯"——后者对提高文章质量更有意义。中文版 stop-slop-zh 针对中文 AI 腔做了本地化。

## 核心内容

### 思路

- 把 AI 高频套路整理成规则：过度铺垫、虚假转折、机械总结、强行制造金句、过度使用连接方式、高度对称句式。
- 定位：**清理坏习惯**，而非**判断是否 AI 生成**（这是它与 AI Detector 的本质区别）。

### 英文版

- 项目：https://github.com/hardikpandya/stop-slop （作者 Hardik Pandya，MIT 协议，约 5.4k+ stars）
- 安装：`npx skills add hardikpandya/stop-slop`
- 核心是一个 62 行的 Markdown 规则文件（SKILL.md + references），把 AI 高频套路列成检查清单，配合五维评分（直接性/节奏/可信度/真实感/密度，满分 50，35 分以下须修改）。

### 中文版 stop-slop-zh

- 针对中文大模型的典型毛病：四字词堆积、过度排比、"不是…而是…"、"从…到…"、"既…又…"、连续总结、名词化表达、宣传稿腔、公文腔。
- 适合写公众号、知乎、小红书、X 中文内容、中文教程、中文商业文章的人。
- ⚠️ **无唯一官方版本**，存在多个独立改编仓库。**按社区口碑（star 数）与官方社区关联，主推：**
  - ✅ **主推**：https://github.com/pencil20388-eng/stop-slop-zh
    - 41 stars（4 个同名仓库中最高）；曾在英文原版 hardikpandya/stop-slop 官方 issue 中被提议加入「其他语言」链接，社区认可度最高。
    - 禁词表 + 标点规则 + 结构约束 + 4 层质检；支持 Claude Code / Cursor / Codex CLI。
  - 其余备选（star 较低，信息少）：
    - https://github.com/leeguooooo/stop-slop-zh （10 stars，10 条改写规则 + 5 维评分）
    - https://github.com/y10reo/stop-slop-zh （4 stars，Codex Skill）
    - https://github.com/wdkang123/stop-slop-zh （1 star，中文本土）

### 在工作流中的位置

属于「第一层：去掉最明显的 AI 腔」，与 [[humanizer-zh]]、qu-ai-wei 并列（详见 [[ai写作去味]]）。

## 相关页面

- 概念：[[去ai味]]
- 实体：[[humanizer-zh]]、[[shuorenhua]]、[[writing-style-skill]]、[[nuwa-skill]]
- 主题：[[ai写作去味]]
- 来源：[[去ai味完整实战教程]]

## 来源与待核实问题

- 来源：[[去ai味完整实战教程]]、https://github.com/hardikpandya/stop-slop
- 已确定：stop-slop-zh 按社区口碑主推 `pencil20388-eng/stop-slop-zh`（41 stars 最高、官方 issue 认可）；其余为备选。
- 待核实：各备选仓库的维护活跃度与长期质量。
