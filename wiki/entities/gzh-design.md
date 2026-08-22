---
title: "gzh-design"
type: entity
aliases:
  - "gzh-design-skill"
  - "公众号排版设计"
  - "公众号排版 Skill"
tags:
  - entity
  - 工具
  - 公众号排版
  - 开源项目
sources:
  - "[[手调半小时的公众号排版]]"
  - "https://github.com/isjiamu/gzh-design-skill"
created: 2026-08-18
updated: 2026-08-18
---

# gzh-design

## 摘要

gzh-design 是解决**公众号编辑器兼容性问题**的开源项目（GitHub：isjiamu/gzh-design-skill，AGPL-3.0 协议）。公众号编辑器不是正常浏览器环境，style 标签、CSS 类名、很多布局属性都不能想当然——gzh-design 处理了这堆最恶心的兼容问题，并提供一键复制预览、HTML 检查和主题基础。

## 核心内容

### 能力

- 公众号编辑器兼容性处理（style 标签 / CSS 类名 / 布局属性的特殊约束）。
- 一键复制预览、HTML 检查、主题基础。

### 作者与协议

- 作者：甲木和摸鱼小李（文中所述）。
- 协议：AGPL-3.0。
- 边界（来自 [[wechat-article-pipeline]] 作者的说明）：六套主题换的是配色和排印、文章结构共用；想要每套组件都不同的，直接用原版 gzh-design；其源码未被复制或重新分发，只在运行时调用，使用者需自行安装。

### 关联

- 是 [[wechat-article-pipeline]] 的核心底层依赖之一。
- 在 [[wesight|WeSight]] 插件中也被用于「公众号草稿直推」的多种 AI 排版主题。

## 相关页面

- 主题：[[公众号排版自动化]]
- 工具：[[wechat-article-pipeline]]、[[wesight]]
- 来源：[[手调半小时的公众号排版]]

## 来源与待核实问题

- 来源：[[手调半小时的公众号排版]]、https://github.com/isjiamu/gzh-design-skill
- 待核实：作者「甲木和摸鱼小李」的完整身份、仓库维护状态。
