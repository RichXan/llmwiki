---
title: "Humanizer-zh"
type: entity
aliases:
  - "humanizer-zh"
  - "中文 Humanizer"
tags:
  - entity
  - 工具
  - Skill
  - 去AI味
sources:
  - "[[去ai味完整实战教程]]"
  - "https://github.com/op7418/Humanizer-zh"
  - "https://github.com/blader/humanizer"
created: 2026-08-17
updated: 2026-08-17
---

# Humanizer-zh

## 摘要

Humanizer-zh 是专门处理**中文 AI 腔**的改写型 Skill。与检测类工具不同，它的目标不是判断 AI 概率，而是"你已经有一篇 AI 初稿，把它改得更像正常中文"。

## 核心内容

### 仓库（存在多个同名版本）

- **英文原版 humanizer**：https://github.com/blader/humanizer （约 36k stars，规则来源于维基百科《Signs of AI writing》与 WikiProject AI Cleanup）
- ✅ **中文版主推**：https://github.com/op7418/Humanizer-zh
  - **15481 stars、1047 forks（另两个同名中文版仅 0 和 6 stars），社区口碑绝对领先**，绝大多数评测文章均指向此版本。
  - 内置 24 种中文 AI 写作痕迹扫描规则，分内容/语法/风格/交流四类。
  - 安装（Claude Code）：`npx skills add https://github.com/op7418/Humanizer-zh.git`
- 其余同名中文版（star 极低，不推荐优先）：
  - https://github.com/WoolenWang/humanizer-zh （0 stars，兼容 Codex / Claude Code / OpenClaw）
  - https://github.com/idao-cube/humanizer-zh （6 stars）

### 重点处理

- 模板化表达、翻译腔、报告腔、过度正式。
- 空泛总结、机械结构、句式高度一致。
- 内置规则举例：过度拔高意义、宣传式语言、模糊归因、否定式排比、三段式法则、破折号滥用、谄媚语气等。

### 定位

- 属于"改写"而非"检测"，比检测 AI 概率实用得多。
- 适合场景：已有 AI 初稿，需要整体去 AI 化。
- 二次审核（Audit）机制：首次改写后再检查残留 AI 痕迹并二次优化。

### 注意（来自原文的重要告诫）

- 很多 Humanizer 为了"人味"会编造经历（如把"配置麻烦"改成"我折腾了三小时差点砸电脑"）——这是**编造事实**，不是 Humanize。没有真实经历应"宁愿不写"。
- 实测反馈（来自评测文章）：规则匹配式改写，偶尔会"矫正过度"，创意/小说类文本慎用，可能把个人风格也当 AI 味改掉。

### 在工作流中的位置

属于「第一层：去掉最明显的 AI 腔」与「第三步：中文重写」，与 [[stop-slop]]、qu-ai-wei、[[shuorenhua]] 配合（详见 [[ai写作去味]]）。

## 相关页面

- 概念：[[去ai味]]
- 实体：[[stop-slop]]、[[shuorenhua]]、[[writing-style-skill]]
- 主题：[[ai写作去味]]
- 来源：[[去ai味完整实战教程]]

## 来源与待核实问题

- 来源：[[去ai味完整实战教程]]、https://github.com/op7418/Humanizer-zh 、https://github.com/blader/humanizer
- 已确定：中文版按社区口碑主推 `op7418/Humanizer-zh`（15481 stars 绝对领先）；WoolenWang / idao-cube 为低 star 备选。
- 待核实：op7418 版最后 push 为 2026-01-19，长期维护活跃度需留意。
