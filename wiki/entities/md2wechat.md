---
title: "md2wechat"
type: entity
aliases:
  - "md2wechat-skill"
  - "极客杰尼"
tags:
  - entity
  - 工具
  - 公众号排版
  - 开源项目
  - 商业授权
sources:
  - "[[手调半小时的公众号排版]]"
  - "https://github.com/geekjourneyx/md2wechat-skill"
created: 2026-08-18
updated: 2026-08-18
---

# md2wechat

## 摘要

md2wechat 是面向 AI Agent 的微信公众号创作与发布 CLI（GitHub：geekjourneyx/md2wechat-skill，作者极客杰尼）。它把公众号发布流程拆成一组可验证的命令：Markdown 转微信 HTML、发布前检查、素材上传、草稿创建，并支持 Claude Code、Codex、WorkBuddy 等 Agent 稳定调用。

## 核心内容

### 主要命令

- `inspect`：解析文章元数据与发布 readiness（推荐 convert 前先跑）。
- `preview`：生成本地预览 HTML，不触发上传或草稿副作用。
- `convert`：Markdown → 微信格式 HTML，可选 `--draft` 直接推送草稿箱。
- `write` / `humanize` / `title suggest` / `generate_cover` / `generate_infographic`：内容生产与 AI 配图。
- `upload_image`：上传图片到微信永久素材库。

### 能力规模

- 48 个专业主题、68 个排版场景条目、53 个 `:::` 语法模块。
- 多账号管理（命名公众号账号，本地只读发现，不输出 Secret）。
- Agent 自动化：通过 JSON discovery 接口供 Claude Code / Codex / WorkBuddy / Kimi Work / Hermes / OpenClaw 调用。

### 协议与商业授权（重要）

- 协议：**BUSL-1.1**（Source Available License，中英双语）。
- 免费范围：个人使用、学习、评估、非营利。
- 需授权范围：商业使用、SaaS、客户交付、白标、再分发、AI 训练数据。
- 2030-01-01 起自动转为 Apache 2.0。
- 微信流量主广告收入视为非商业用途（免费）。
- 专业 API 模式需 md2wechat API Key（免费 AI 模式仅 3 个基础主题，API 模式 48 个专业主题）。

### 作者

- 极客杰尼 = GitHub `geekjourneyx` = X `@seekjourney`（同一人，经 GitHub 主页与多个公开来源核实）。
- 背景：十多年程序员经验，白天在北京互联网大厂做后端架构，晚上做 AI Agent 与独立产品；个人站点 jieni.ai，公众号「极客杰尼」。
- 仓库约 3.3k stars；周边生态：obsidian-md2wechat、md2wechat-mcp-server、feishu-md2wechat 等。

## 相关页面

- 主题：[[公众号排版自动化]]
- 流水线：[[wechat-article-pipeline]]
- 底层：[[gzh-design]]
- 来源：[[手调半小时的公众号排版]]

## 来源与待核实问题

- 来源：[[手调半小时的公众号排版]]、https://github.com/geekjourneyx/md2wechat-skill
- ✅ 已确认：作者「极客杰尼」= GitHub `geekjourneyx` = X `@seekjourney`，为同一人。
- ⏳ 待核实：BUSL-1.1 商业授权的最新条款细节以仓库 LICENSE 为准（存在 fork 版本标注 MIT，属历史/镜像差异）。
