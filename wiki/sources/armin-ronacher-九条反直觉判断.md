---
title: "Pi Agent 作者 Armin Ronacher 谈 agent 未来：九条反直觉判断"
type: source
aliases:
  - "Armin Ronacher 九条反直觉判断"
  - "Pi Agent 与 agent 未来"
tags:
  - source
  - article
  - Agent
  - harness
  - 开源
sources:
  - "[[raw/articles/Pi Agent 作者 Armin Ronacher 谈 agent 未来：九条反直觉判断]]"
created: 2026-09-15
updated: 2026-09-15
---

# 来源摘要：Armin Ronacher 谈 agent 未来的九条反直觉判断

## 摘要

[[justin-1024go|@Justin1024go]] 摘录整理的九条观点（原访谈为 YouTube 视频），源自 **[[armin-ronacher|Armin Ronacher]]**（Flask / Jinja 作者，[[earendil|Earendil]] 联合创始人，Pi 项目核心维护者）。核心立场：**agent 还处在 DOS 时代**，缺的不是算力而是持久性、Web 原生体验与数据层；harness 竞争正在收敛到"基础功"（极简 + bash）；很多"AI 问题"其实是系统架构问题；人类不会退场，因为机器不可问责。

> ⚠️ **标题准确性说明**：原文标题称其为"**Pi Agent 作者**"。据 2026-09-15 网络检索，**Pi 的原创作者是 Mario Zechner（libGDX 作者）**，2026-04 由 Earendil 收购后，Ronacher 与 Zechner、Colin 共同主导技术方向。Ronacher 是 Pi 的**核心使用者与维护者**，称"作者"不够准确，**已在本库标注该分歧**（详见 [[armin-ronacher]] 与 [[pi-agent]]）。

## 元信息

- **摘录整理者**：[[justin-1024go|@Justin1024go]]（身份待核实）
- **观点来源**：Armin Ronacher 原访谈（YouTube：https://www.youtube.com/watch?v=SxuQs9GGYbk）
- **发布**：2026-09-14
- **原始链接**：https://x.com/Justin1024go/status/2099514598449975525
- **原始文件**：`[[raw/articles/Pi Agent 作者 Armin Ronacher 谈 agent 未来：九条反直觉判断]]`
- **入库日期**：2026-09-15

## 核心内容

### 01｜极简为什么能赢

- 所有 harness 的竞争都在收敛到「基础功」，因为**模型自己越来越会用电脑**。
- "Pi 基本上只给你一个 **bash**"——而 bash 管道恰恰是**最省上下文**的形态。
- 反直觉的是：工具看似繁多的 [[codex|Codex]]，底层也在大量调用 bash。
- 关联：[[harness-极简主义]]、[[skill文件]]（渐进披露）

### 02｜agent 还处在 DOS 时代

> 「现在的 agent，基本还不是任何人真正该用的界面。我很难想象 4 年后我们还在用今天这个形态的 coding agent。」

- 缺的不是算力，而是三样：**持久性**（可挂起、可恢复）、**Web 原生的体验**、**agent 自己的数据层**。

### 03｜很多「AI 问题」其实是系统架构问题

- 「**对人是便宜的事，对 agent 是贵的，反之亦然。**」
- agent 支不起持久的自定义 UI、不敢让它直接操作数据——需要的是**状态管理、组件库、数据层设计**，而不是新的 AI 突破。
- 副产品判断：**Linux 会复兴**。"我妈用 agent 定制 Linux，可能比定制 Mac 更成功。"

### 04｜人类不会退场

- 「你得能怪到某个人头上，**机器不可问责**——社会不会这么运转。」所以银行不会 vibe code。
- **可内省性是刚需**：人要能亲眼看 agent 哪里没搞懂，而不是去问一个可能撒谎的 agent。
- 这也是 **Markdown、JSON、Unix 管道在赢**的原因：**人能看懂**。

### 05｜开源 = 进入训练数据的门票

- 「想让 agent 来构建你的东西？开源有天然优势——**它会进入训练数据**。」
- 他评判开源项目只用一个问题：**10–15 年后，它还在吗？还开源吗？**
- "早期 PHP 糟透了，但它活下来了——今天它是一门好语言。"

### 06｜企业买 AI 编码，账还没算清

- 「企业花了这么多钱在 AI 编码上——**收入真的上去了吗？**」
- 他观察到：**commit 数量爆炸**、GitHub 都快撑不住，但社会层面的变化远小于预期。
- 「**成本的显现比收益快得多。**」

### 07｜他自己的工作流：保守到自嘲

- 本地为主、一台 SSH 开发机跑常驻任务、GitHub Actions 跑一点自动化。
- 自嘲：Earendil 可能是唯一没有「自动修 issue 机器人」的 harness 公司——「**不是没试过软件工厂，是没成功**」。

### 08｜关于烧钱，与最坏的结局

- 「如果按 API 价格付费，我根本不会怎么用 AI——**那等于烧投资人的钱**。」
- 他最怕的结局：**AI 像社交媒体一样，人人都在用、同时人人都在恨。**

### 09｜欧洲为什么掉队

- 「欧洲的主题是**保存过去**，而不是启用未来。」
- 根子在于「**欧洲不是一个国家**」——27 套法律、27 种摩擦，有动力的人正在离开。

## 相关页面

- 概念：[[harness-极简主义]]、[[可内省性]]、[[skill文件]]
- 实体：[[armin-ronacher]]、[[pi-agent]]、[[earendil]]、[[codex]]、[[claude-code]]
- 主题：[[agent工程]]、[[ai原生软件开发]]
- 对照来源：[[agent工程解析-上下文管理]]（同为 agent 工程视角）

## 来源与待核实问题

- **来源**：https://x.com/Justin1024go/status/2099514598449975525 （原访谈 https://www.youtube.com/watch?v=SxuQs9GGYbk）

### 待核实

- **标题表述**："Pi Agent 作者"与事实不符（Pi 原创作者为 Mario Zechner），已标注分歧。
- 原访谈视频**未逐字核对**，本页内容基于摘录帖的转述，可能存在语境损失；九条的编号与措辞以摘录者整理为准。
- 摘录者 @Justin1024go 身份。
- 文中数字（如 "commit 数量爆炸"）为定性描述，无具体数据。
- 第 07 条提到的"Earendil 唯一没有自动修 issue 机器人"为自嘲式表述，未核实。
- 第 08 条"按 API 价格付费"具体所指（对比 Cursor Ultra 等订阅）未明说。
