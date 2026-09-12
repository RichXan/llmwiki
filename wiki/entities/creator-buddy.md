---
title: "creator-buddy"
type: entity
aliases:
  - "creator-buddy Skills"
  - "gzh-Skills"
  - "公众号写作Skill合集"
tags:
  - entity
  - 工具
  - Skill
  - 公众号
sources:
  - "[[10个skill搭建公众号写作系统]]"
created: 2026-09-12
updated: 2026-09-12
---

# 实体：creator-buddy

## 摘要

**creator-buddy** 是作者 [@kongge_space](https://x.com/kongge_space) 开源的一套创作者工具集，其 `gzh-Skills` 目录下收纳了 **10 个公众号写作 Skill**，覆盖账号定位、选题、写作、标题、配图、封面与排版全流程。作者主张把公众号创作拆成可复用的 Skill，让 AI 承担流程性工作、人专注在选题与判断上（详见 [[公众号内容创作系统]]）。

## 核心内容

### 基本信息

- **仓库地址**：https://github.com/SpaceZephyr/creator-buddy/tree/main/gzh-Skills
- **GitHub 账号**：SpaceZephyr
- **作者**：@kongge_space（X）
- **来源**：[[10个skill搭建公众号写作系统]]（2026-08-27）
- **形态**：一套编排在同一仓库下的 Skill，而非单点工具

### 十个 Skill 一览

| 组别 | Skill | 职责 | 关键细节 |
| --- | --- | --- | --- |
| 定位与选题 | `gzh-positioning` | 账号定位 | 一句话收敛定位，生成简介、关注回复与菜单 |
| 定位与选题 | `baokuan-article-analysis` | 爆款分析 | 按赛道抓公众号爆款，用真实数据找选题方向 |
| 定位与选题 | `gzh-explosive-content-detector` | 每日爆款 | 持续收录"低粉高阅读"文章，提供最真实的数据参考 |
| 写作 | `gzh-longform-writer` | 长文写作 | 先询问手上素材，按素材形态路由**六种写法** |
| 写作 | `gzh-short-post` | 短文写作 | 千字以内纯文字推送，自带**去 AI 腔风格规则与输出自检** |
| 写作 | `baokuan-title-generator` | 爆款标题 | 批量生成候选，逐个评分标风险，按场景推荐 |
| 配图与封面 | `space-gzh-cover` | 头图封面 | **2.35:1** 封面，带**分享安全区校验**防止标题被裁切 |
| 配图与封面 | `space-chart-image` | 图表配图 | 十类图表：流程图、架构图、思维导图、SWOT 等 |
| 配图与封面 | `space-text-logic-diagram` | 逻辑配图 | 把段落拆成逻辑关系图，**六种关系类型** |
| 排版 | `space-wechat-layout` | 整篇排版 | 文章转公众号 HTML，一键复制粘贴进编辑器 |

### 在创作流程中的位置

- 与 [[wechat-article-pipeline]]（[[davinci-seven|达芬七]]的流水线）同属"公众号自动化"工具，但侧重点不同：creator-buddy 覆盖**上游创作**，wechat-article-pipeline 聚焦**下游排版发布**。
- `space-wechat-layout` 与 [[gzh-design]]、[[xiaowan-wechat-layout]]、[[md2wechat]] 属同类"Markdown → 公众号 HTML"能力，可对照 [[公众号排版自动化]]。
- `gzh-short-post` 的去 AI 腔能力与 [[ai写作去味]] 主题相关。

## 相关页面

- 主题：[[公众号内容创作系统]]、[[公众号排版自动化]]、[[ai写作去味]]
- 实体（同类工具）：[[wechat-article-pipeline]]、[[gzh-design]]、[[xiaowan-wechat-layout]]、[[md2wechat]]
- 来源：[[10个skill搭建公众号写作系统]]

## 来源与待核实问题

- **来源**：[[10个skill搭建公众号写作系统]]
- **待核实**：
  - 仓库 **LICENSE**、各 Skill 是否已完整开源、最近提交与维护状态（本次未做网络检索）。
  - GitHub 账号 `SpaceZephyr` 与 X 账号 `@kongge_space` 是否同一人。
  - 作者 @kongge_space 的真实身份。
  - 文中列出的"10 个"以文章自述为准，仓库实际内容可能更多或其他。
