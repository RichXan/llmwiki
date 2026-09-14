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

**creator-buddy** 是作者**空格.space**（X：[@kongge_space](https://x.com/kongge_space)，GitHub `SpaceZephyr`）开源的一套创作者工具集，覆盖公众号、小红书、视频三条创作链。其中 `gzh-Skills` 目录收纳公众号写作 Skill（帖子列举 10 个，目录实测 12 个），覆盖账号定位、选题、写作、标题、配图、封面与排版全流程。作者主张把创作拆成可复用的 Skill，让 AI 承担流程性工作、人专注在选题与判断上（详见 [[公众号内容创作系统]]）。

## 核心内容

### 基本信息

- **仓库地址**：https://github.com/SpaceZephyr/creator-buddy
- **GitHub 账号**：SpaceZephyr（名称「空格的键盘」）
- **作者**：空格.space（X：[@kongge_space](https://x.com/kongge_space)）
- **来源**：[[10个skill搭建公众号写作系统]]（2026-08-27）
- **形态**：一套编排在同一仓库下的 Skill 集合，而非单点工具
- **三条产品线**：`gzh-Skills/`（公众号）、`xhs-Skills/`（小红书，10 个 Skill）、`video-Skills/`（视频：选题→脚本→剪辑→B-roll→字幕→配音→封面）
- **协议**：README 与根 SKILL.md 声明 **MIT**；但**仓库根目录未提供可识别的 LICENSE 文件**（待作者补充）
- **安装**：`npx skills add SpaceZephyr/creator-buddy`（基于开放 Agent Skills 协议，支持 Claude Code / Codex / Cursor 等）
- **热度快照**：2026-08-27 约 758 stars / 117 forks
- **使用边界**：只读公开数据，**不代执行发布、点赞、评论等账号动作**；AI 生成的封面与配图仍需人工检查

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

> 目录实测另有 `global-content-search`（跨平台内容搜索）与 `xhs-hotnotes`（小红书热搜）两个 Skill，因此 `gzh-Skills/` 实际为 **12 个**；上表为帖子列举的 10 个核心 Skill。

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

### 已核实（网络检索，2026-09-12）

- GitHub `SpaceZephyr` 与 X `@kongge_space` 为同一人（作者名「空格.space」，GitHub 名称「空格的键盘」）。
- 仓库确含三条产品线（公众号 / 小红书 / 视频），安装命令为 `npx skills add SpaceZephyr/creator-buddy`。
- 2026-08-27 热度快照约 758 stars / 117 forks。
- 第三方衍生：摸鱼局长（@Jason23818126）于 2026-08-30 发布 **GZH Buddy**（agent.creao.ai，v1.0.0），系对 gzh-Skills 的封装。

### 仍需人工确认

- **协议**：声明 MIT 但根目录无 LICENSE 文件，实际授权待作者补充。
- **维护状态**：最近提交时间与本页信息时效性需后续复查。
- 帖子"10 个"与目录"12 个"的差异属正常范围（另两个为跨平台/小红书 Skill），已在上文注明。
