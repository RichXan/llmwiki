---
title: "shuorenhua"
type: entity
aliases:
  - "说人话"
  - "shuorenhua Skill"
tags:
  - entity
  - 工具
  - Skill
  - 去AI味
sources:
  - "[[去ai味完整实战教程]]"
  - "https://github.com/MrGeDiao/shuorenhua"
created: 2026-08-17
updated: 2026-08-17
---

# shuorenhua

## 摘要

shuorenhua（「说人话」）是让 AI 输出按**真实场景**切换表达方式的 [[去ai味|去 AI 味]] Skill。核心思路：同一句话在不同场景下本来就不该用同一种表达——人在不同场景下本来就不会使用同一种语言。

## 核心内容

### 仓库（存在多个同名版本）

- ✅ **主推**：https://github.com/MrGeDiao/shuorenhua
  - **1098 stars、61 forks（另两个同名版本仅 0 和 9 stars），且截至 2026-08-17 仍在活跃更新**，社区口碑与维护度最高。
  - 安装（Claude Code）：`npx skills add MrGeDiao/shuorenhua`
  - 定位：中文优先的去 AI 味改写，保事实、分场景；核心只需 `SKILL.md`（lite），长期项目建议带上 `references/`（full）。
- 其余同名版本（star 极低，不推荐优先）：
  - https://github.com/Jia-Hong-Peng/shuorenhua （0 stars，文档较全，附 benchmark 与误杀防护）
  - https://github.com/1-SKILL/shuorenhua （9 stars，偏论文降重）

### 核心思路

- 事实不变，表达方式随场景切换。
- 例：原句"该产品能够有效提高用户的内容生产效率"——
  - 产品介绍："它主要帮你省掉查资料、整理素材和写第一稿这些重复工作。"
  - 发 X："AI 真正帮我省下来的，不是打字时间，而是查资料和整理资料的时间。"
  - 跟老板汇报："目前测试下来，它对第一版内容生产时间的压缩最明显。"
- 处理对象：工程师腔、AI 腔、小红书模板腔、翻译腔、无来源的权威表达；强调改写中保护事实、版本、命令和证据。

### 定位

- 属于「第二层：把文字改成正常人会说的话」。
- 解决的是"别只写正确的话，要写自然的话"（区别于 [[humanizer-zh]] 的"别一眼 AI"）。
- 明确"不是拿来骗 AI 检测器的"，目标是减少模板感、表演感和语域漂移。

## 相关页面

- 概念：[[去ai味]]
- 实体：[[stop-slop]]、[[humanizer-zh]]、[[writing-style-skill]]
- 主题：[[ai写作去味]]
- 来源：[[去ai味完整实战教程]]

## 来源与待核实问题

- 来源：[[去ai味完整实战教程]]、https://github.com/MrGeDiao/shuorenhua
- 已确定：按社区口碑主推 `MrGeDiao/shuorenhua`（1098 stars 最高、仍在活跃维护）；Jia-Hong-Peng / 1-SKILL 为低 star 备选。
