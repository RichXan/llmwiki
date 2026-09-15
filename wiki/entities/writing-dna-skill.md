---
title: "writing-dna-skill"
type: entity
aliases:
  - "writing-dna-skill"
  - "写作蒸馏器"
  - "Writing DNA Distiller"
  - "语言DNA.md"
tags:
  - entity
  - Skill
  - 工具
  - AI写作
  - 开源
sources:
  - "[[去ai味语料实证研究]]"
created: 2026-09-15
updated: 2026-09-15
verified: 2026-09-15
---

# 实体：writing-dna-skill

## 摘要

**writing-dna-skill**（"写作蒸馏器"）是 [[lieflat-less-ai-tone]] 作者 `larashero3-dotcom`（GitHub 显示名 "lieflat"）的另一个开源 Skill——**"蒸馏复刻任意写作风格的 agent skill"**（仓库 `larashero3-dotcom/writing-dna-skill`，**MIT，1,832★ / 180 forks**）。

它在本库中的意义有两层：① 它是 [[ai写作去味]] 主题「**三条技术路线**」中 **Skill 组合派** 的一个新样本；② 更重要的是——**它内置了 [[lieflat-less-ai-tone]] 的规则集**，使该主题出现了**首次"两条路线在同一产品内协同"**的实现。

## 核心内容

### 基本信息

| 维度 | 信息 |
| --- | --- |
| **仓库** | https://github.com/larashero3-dotcom/writing-dna-skill |
| **中文名** | 写作蒸馏器 |
| **定位（官方描述）** | "蒸馏复刻任意写作风格的 agent skill / Writing DNA Distiller - distill and recreate any writing style as an agent skill" |
| **协议** | **MIT** |
| **仓库指标（2026-09-15 GitHub API）** | ⭐ **1,832** stars / **180** forks；创建 **2026-06-27**；最后推送 **2026-08-24**；**无主语言标记**（应为纯 Markdown/Prompt 资产）；topics：`ai-agent`、`skill`、`style-analysis`、`writing`、`writing-dna` |
| **产物命名** | 蒸馏产物名为 **`语言DNA.md`**（[[lieflat-less-ai-tone]] 的 SKILL.md 中提及） |

### 与 [[lieflat-less-ai-tone]] 的关系（SKILL.md 原文）

> "与写作风格蒸馏配合使用时不必单独安装本规则集，[writing-dna-skill](https://github.com/larashero3-dotcom/writing-dna-skill) **已内置一份**，装该仓库即随行。"

**两者构成两道工序**（原文）：

| 工序 | 承担者 | 职责 |
| --- | --- | --- |
| **第一道** | `writing-dna-skill` | **风格逼近**——蒸馏目标作者的实际写法 |
| **第二道** | [[lieflat-less-ai-tone]] | **清除生成痕迹**——按 11 条白名单规则清理 |

**冲突处理原则**（重要，原文）："同目录存在蒸馏产物时**优先读取 `语言DNA.md`**；两者冲突时**以蒸馏产物为准**，因其记录的是目标作者的实际写法，**不属生成痕迹**。"

> 🔗 **这条原则的意义超出单个项目**：它给出了"**规则派 vs 样本派**"之争的一个具体裁决机制——**当规则与真实样本冲突时，样本优先**。这与 [[ai写作去味]] 主题中「真实样本派」的核心主张一致，但**不同在于：这里并不否定规则，而是给规则划定了"样本优先"的边界**。
>
> 换言之，`writing-dna-skill` 是 [[ai写作去味]] 中**前两条路线首次在同一产品内被打通**的实现——**它同时是本库"两条路线并用"这一务实建议的现成样本**。

### 举例（SKILL.md 的用法示例）

原文举的例子说明了"样本优先"如何生效：

> "比如某作者本来就爱用破折号，就不该按第 4 条删掉。"

——即：**破折号是显著的 AI 特征（*R*=3.0），但若蒸馏产物显示该目标作者本人就爱用破折号，则该规则对该作者失效。** 这是"实证派 + 样本派"协同的一个具体决策例。

### 同作者的方法论产品线（已核实）

| 仓库 | 说明 | ★ / forks |
| --- | --- | --- |
| `lieflat-charts` | 面向 Agent 的数据可视化 Skill（HTML 图表） | 5,384 / 327 |
| **`writing-dna-skill`** | **写作蒸馏器（本页）** | **1,832 / 180** |
| `lieflat-gongwen` | **102 万字语料**提炼的公文写作 Skill——"把公文写作风格变成可测量、可验收的量化数据" | 961 / 148 |
| [[lieflat-less-ai-tone]] | 283 万字语料的去 AI 味 Skill | 780 / 56 |
| `lieflat-html-design` | Agent 用 HTML 设计 Skill 集 | 87 / 3 |
| `soul.skill` | 复刻他人思维方式为 AI 人格 | 49 / 6 |

> 📌 `writing-dna-skill` **star 数是本系列最高的写作类项目**（1,832），且**早于** `lieflat-less-ai-tone`（2026-06-27 vs 2026-08-20）——即**"蒸馏风格"先做，"清除 AI 痕迹"后做**，二者是配套演进的。

## 相关页面

- 实体：[[lieflat-less-ai-tone]]（配套工序）、[[writing-style-skill]]（同类对照）、[[chatgpt]]（真实样本派的平台实现）
- 概念：[[个人写作风格库]]、[[ai味特征实证]]、[[去ai味]]
- 主题：[[ai写作去味]]
- 来源：[[去ai味语料实证研究]]

## 来源与待核实问题

- **来源**：
  - 原始来源：[[去ai味语料实证研究]]（未提及本仓库）
  - 网络核实（2026-09-15）：GitHub API（`stargazers_count` **1,832**、`forks_count` **180**、`created_at` **2026-06-27T14:43:12Z**、`pushed_at` **2026-08-24T06:57:16Z**、`license.spdx_id` **MIT**）
  - 交叉来源：[[lieflat-less-ai-tone]] 的 `SKILL.md`（"已内置一份""以蒸馏产物为准"）

### 待核实

- **README 与 SKILL.md 未读取**：本页信息主要来自 **GitHub API 元数据 + [[lieflat-less-ai-tone]] 中提及本仓库的段落**。**蒸馏方法（用什么语料、如何提取"语言DNA"）、产出的 `语言DNA.md` 格式、蒸馏质量**均未核实。
- **"已内置一份规则集"的具体形式**（是硬编码进 SKILL.md、作为独立文件、还是动态引用）——**未打开仓库验证**。
- **1,832★ 与较低 fork 数（180）的组合**提示可能为"收藏多于使用"，但无证据，**不作判断**。
- **作者身份**同 [[lieflat-less-ai-tone]]：GitHub "lieflat"，与 X @Zhiyu333 的对应关系未直接证实。
- **与 [[writing-style-skill]] 的差异**（同为"从真实文本提炼文风"的 Skill 形态）——**两者未做对照测试**，本页只记录并存，**不比较优劣**。
- **仓库无主语言标记**，可能为纯 Markdown/Prompt 资产——未验证。
