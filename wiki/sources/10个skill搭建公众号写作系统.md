---
title: "10 个 Skill 搭建日更爆文的公众号写作系统"
type: source
aliases:
  - "10个Skill公众号写作系统"
  - "公众号写作Skill系统"
  - "日更爆文写作系统"
tags:
  - source
  - article
  - 公众号
  - AI写作
  - 工具
sources:
  - "[[raw/articles/10 个 Skill 搭建日更爆文的公众号写作系统]]"
created: 2026-09-12
updated: 2026-09-12
---

# 来源摘要：10 个 Skill 搭建日更爆文的公众号写作系统

## 摘要

本文作者（X：@kongge_space）自述做公众号三年、约三万粉、近半年月入一两万，分享了自己把公众号创作全流程（选题 → 写作 → 配图 → 排版 → 分发）拆成 **10 个 Skill** 的做法，并开源在同一仓库 [[creator-buddy]] 下。文章先讲公众号的商业化逻辑（为什么报价高于小红书/抖音），再给出每个 Skill 的职责、作者自己的六步创作流程，以及"50% 靠选题、30% 拼标题封面、20% 才是把话捋顺"的权重判断。

## 元信息

- **作者**：空格.space（X：[@kongge_space](https://x.com/kongge_space)；GitHub 名称「空格的键盘」，已核实）
- **发布日期**：2026-08-27
- **原始链接**：https://x.com/kongge_space/status/2092902850821337330
- **原始文件**：`[[raw/articles/10 个 Skill 搭建日更爆文的公众号写作系统]]`
- **入库日期**：2026-09-12

## 核心内容

### 1. 公众号的商业化逻辑

- **报价逻辑**：平均阅读量 × 2；一万阅读约可报价两万，但要做到平均一万阅读，至少需十万粉以上。
- **为什么更值钱**：读者中创业者、老板多，决策力与消费力强；微信的触达能力与原创保护让文章持续积累信用。
- **平台差异**：小红书、抖音像"广场"，公众号像"自己的房间"，读者会坐下来认真读，更容易建立长期关系。
- **起号现状**：推荐机制对新人更友好，选题准、爆一两篇就能起量，但很难靠单篇爆款涨粉过万，需稳扎稳打、按年经营。

### 2. 十个 Skill（分四组）

| 组别 | Skill | 职责 |
| --- | --- | --- |
| 定位与选题 | `gzh-positioning` | 账号定位：一句话收敛定位，生成简介、关注回复、菜单 |
| 定位与选题 | `baokuan-article-analysis` | 爆款分析：按赛道抓公众号爆款，用真实数据找选题方向 |
| 定位与选题 | `gzh-explosive-content-detector` | 每日爆款：持续收录低粉高阅读文章 |
| 写作 | `gzh-longform-writer` | 长文写作：先问手上有什么素材，按素材形态路由六种写法 |
| 写作 | `gzh-short-post` | 短文写作：千字以内纯文字推送，带去 AI 腔风格规则与输出自检 |
| 写作 | `baokuan-title-generator` | 爆款标题：批量生成候选，逐个评分标风险，按场景推荐 |
| 配图与封面 | `space-gzh-cover` | 头图封面：2.35:1，带分享安全区校验（防标题被裁切） |
| 配图与封面 | `space-chart-image` | 图表配图：十类图表（流程图、架构图、思维导图、SWOT 等） |
| 配图与封面 | `space-text-logic-diagram` | 逻辑配图：把段落拆成六种逻辑关系图 |
| 排版 | `space-wechat-layout` | 整篇排版：文章转公众号 HTML，一键复制粘贴 |

> 详见实体页 [[creator-buddy]]。

### 3. 作者的六步创作流程

1. **灵感记录**：语音输入法说一遍发给文件传输助手；或快速手写、不懂的概念先用 `xxx` 占位。核心是**把"想"和"写"分开**。
2. **选题验证**：用 `baokuan-article-analysis` 跑赛道关键词，再用 `gzh-explosive-content-detector` 看高阅读文章的选题与风格。
3. **写作**：**完形填空式**——一口气写出结构或语音念出，卡壳处打 `xxx` 保持思路惯性，写完让 `gzh-longform-writer` 填充、自己再改。原则是**人定骨架，AI 填肉**：观点、结构、起承转合必须是作者的。
4. **标题**：`baokuan-title-generator` 批量出候选并评分标注风险，挑两三个自己再改一版。
5. **配图与封面**：用支持生图的 Agent（如 [[codex]]）调用 `space-chart-image`、`space-text-logic-diagram` 出图；`space-gzh-cover` 出封面并做安全区校验。
6. **排版发布**：`space-wechat-layout` 转 HTML 后复制进后台；作者另做了把飞书推送文章自动转小红书图文/公众号排版的插件。习惯让草稿多放两天再读。发布后再录成视频分发到 B 站、小红书、知乎等。

### 4. 关键判断与方法

- **权重公式**：50% 靠选题，30% 拼封面和标题，20% 才是把话捋顺；很多人把 50% 的精力花在了 20% 上。
- **灵感观**：选题源于灵感，灵感本质是"身心状态"与"日常信息输入"的综合反应；创作第一步是睡好觉。
- **工具清单**：语音输入（微信/豆包输入法）、AI 写作（Claude、[[codex]]、豆包）、配图（Codex、NotebookLM、豆包）、内容管理（[[obsidian]]、飞书）、编辑发布（飞书排版插件、一键发布插件）、录屏剪辑（Screen Studio + 剪映）。

### 5. 开源地址

- Skill 仓库：https://github.com/SpaceZephyr/creator-buddy/tree/main/gzh-Skills

## 相关页面

- 实体：[[creator-buddy]]、[[codex]]、[[obsidian]]
- 主题：[[公众号内容创作系统]]、[[公众号排版自动化]]、[[ai写作去味]]
- 工具（关联）：[[wechat-article-pipeline]]、[[wesight]]

## 来源与待核实问题

- **来源**：https://x.com/kongge_space/status/2092902850821337330

### 已核实（网络检索，2026-09-12）

- **作者**：空格.space（[@kongge_space](https://x.com/kongge_space)），GitHub 账号 `SpaceZephyr`（名称「空格的键盘」），即该创作者工具集的作者。
- **仓库**：`SpaceZephyr/creator-buddy` 确认存在，含三条产品线——`gzh-Skills/`（公众号）、`xhs-Skills/`（小红书）、`video-Skills/`（视频）。README 与根 SKILL.md 声明 **MIT**，但**仓库根目录未提供可识别的 LICENSE 文件**。
- **热度快照**：2026-08-27 采集时约 **758 stars / 117 forks**；作者原帖约 114.3K 浏览、912 赞、163 转发。
- **Skill 数量修正**：`gzh-Skills/` 目录实测有 **12 个 Skill**，比文中"10 个"多出 `global-content-search` 与 `xhs-hotnotes`（后者属跨平台热搜）。文中"10 个"是作者帖子里列举的核心集合，并非目录全量。
- **安装与边界**：安装命令 `npx skills add SpaceZephyr/creator-buddy`（基于开放 Agent Skills 协议，支持 Claude Code / Codex / Cursor 等 runtime）。仓库明确**只读公开数据，不代执行发帖/点赞/评论等账号动作**；热点流程依赖外部数据服务，无服务时回退公开搜索。
- **衍生项目**：摸鱼局长（@Jason23818126）于 2026-08-30 将其封装为 **GZH Buddy**（安装页 agent.creao.ai，Version 1.0.0），属第三方封装传播，非原作者出品。
- **细节补充**：`baokuan-title-generator` 含 **16 种爆款标题方法**（评分 + A/B）；`gzh-positioning` 带微信硬约束（简介 4–120 字、关注后回复 ≤600 字、一级菜单 ≤4 汉字、二级菜单 ≤8 汉字）与"从历史文章反推定位"。

### 仍需人工确认

- "做公众号三年、三万粉、近半年月入一两万"仍为作者自述，无第三方验证。
- 报价公式"平均阅读量 × 2"与收入数字属作者个人经验，非普适结论，读者不宜直接套用。
- 仓库声明 MIT 但根目录无 LICENSE 文件，实际授权以作者后续补充为准。
