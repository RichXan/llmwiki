---
title: "xiaowan-wechat-layout"
type: entity
aliases:
  - "xiaowan-wechat-layout-skill"
  - "小晚公众号排版"
  - "公众号排版 Lite"
tags:
  - entity
  - 工具
  - 公众号排版
  - 开源项目
sources:
  - "[[手调半小时的公众号排版]]"
  - "https://github.com/cyberxiaowan/xiaowan-wechat-layout-skill"
created: 2026-08-18
updated: 2026-08-18
---

# xiaowan-wechat-layout

## 摘要

xiaowan-wechat-layout 是 [[gzh-design]] 的**工作流增强层**（GitHub：cyberxiaowan/xiaowan-wechat-layout-skill，AGPL-3.0-or-later）。它不包含公众号 HTML 排版引擎，而是在 gzh-design 生成的 HTML 之上，加入作者 @小晚不在 从真实发布复盘里沉淀的移动端检查、反馈路由和复盘流程。

## 核心内容

### 定位

- 依赖 [[gzh-design]]（需先安装），调用它生成基础公众号 HTML，再加入移动端检查与复盘规则。
- 是「工作流层」，不是排版引擎；不含 gzh-design 源码。

### 重点检查项（排版时）

首屏是否为完整信息单元、大章节是否一眼可见、线条/色块/外框是否过多、标题是否有 2–3 字孤行、重点句是否只高亮半句、图片是否解释正文、多图是否预拼、粘贴后是否丢图/错位、人工调整能否沉淀为可复用规则。

### 默认视觉起点

正文 14px / #595757 / 1.9–2 行距、章节强调赭金 #b17816、背景米白 #fdfdf8，靠层级与留白组织文章，少线条外框。

### 安装

- 方式一：把一段提示词复制给 Codex，一次性装好 gzh-design + 本 Skill。
- 方式二：Mac 一键安装（解压后双击 `install.command`）。

### 作者与协议

- 作者：小晚，网名「@小晚不在」（GitHub：cyberxiaowan，X：[@bbkirstry](https://x.com/bbkirstry)）——三者经核实为同一人。
- 协议：AGPL-3.0-or-later。
- 仓库约 74 stars。

## 相关页面

- 底层：[[gzh-design]]
- 主题：[[公众号排版自动化]]
- 流水线：[[wechat-article-pipeline]]
- 来源：[[手调半小时的公众号排版]]

## 来源与待核实问题

- 来源：[[手调半小时的公众号排版]]、https://github.com/cyberxiaowan/xiaowan-wechat-layout-skill
- ✅ 已确认：作者「小晚」=「@小晚不在」= GitHub `cyberxiaowan` = X `@bbkirstry`，为同一人（GitHub 个人主页明确标注 X 账号 @bbkirstry）。
