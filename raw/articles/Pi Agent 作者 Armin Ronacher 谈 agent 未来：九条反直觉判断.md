---
title: "Pi Agent 作者 Armin Ronacher 谈 agent 未来：九条反直觉判断"
source: "https://x.com/Justin1024go/status/2099514598449975525"
author:
  - "[[@Justin1024go]]"
published: 2026-09-14
created: 2026-09-15
description: "Pi Agent 作者 Armin Ronacher（也是 Flask 的作者）最近有不少关于 agent 的判断，清醒得有点扎心。我挑出最值得细读的九条 👇01｜极简为什么能赢所有 harness 的竞争都在收敛到「基础功」，因为模型自己越来越会用电脑。「Pi 基本上只给你一..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HSL43TTbcAAz-Hp?format=jpg&name=large)

Pi Agent 作者 Armin Ronacher（也是 Flask 的作者）最近有不少关于 agent 的判断，清醒得有点扎心。我挑出最值得细读的九条 👇

01｜极简为什么能赢

所有 harness 的竞争都在收敛到「基础功」，因为模型自己越来越会用电脑。「Pi 基本上只给你一个 bash」——而 bash 管道恰恰是最省上下文的形态。反直觉的是：工具看似繁多的 Codex，底层也在大量调用 bash。

02｜agent 还处在 DOS 时代02｜agent 仍然处于 DOS 时代

「现在的 agent，基本还不是任何人真正该用的界面。我很难想象 4 年后我们还在用今天这个形态的 coding agent。」

他认为缺的不是算力，而是持久性（可挂起、可恢复）、Web 原生的体验、以及 agent 自己的数据层。

03｜很多「AI 问题」其实是系统架构问题

「对人是便宜的事，对 agent 是贵的，反之亦然。」agent 支不起持久的自定义 UI、不敢让它直接操作数据——需要的是状态管理、组件库、数据层设计，而不是新的 AI 突破。

一个副产品判断：Linux 会复兴。「我妈用 agent 定制 Linux，可能比定制 Mac 更成功。」

04｜人类不会退场

「你得能怪到某个人头上，机器不可问责——社会不会这么运转。」所以银行不会 vibe code；可内省性是刚需——人要能亲眼看 agent 哪里没搞懂，而不是去问一个可能撒谎的 agent。这也是 Markdown、JSON、Unix 管道在赢的原因：人能看懂。

05｜开源 = 进入训练数据的门票

「想让 agent 来构建你的东西？开源有天然优势——它会进入训练数据。」他评判一个开源项目只用一个问题：10–15 年后，它还在吗？还开源吗？「早期 PHP 糟透了，但它活下来了——今天它是一门好语言。」

06｜企业买 AI 编码，账还没算清

「企业花了这么多钱在 AI 编码上——收入真的上去了吗？」他看到的是：commit 数量爆炸、GitHub 都快撑不住，但社会层面的变化远小于预期。「成本的显现比收益快得多。」

07｜他自己的工作流：保守到自嘲

本地为主、一台 SSH 开发机跑常驻任务、GitHub Actions 跑一点自动化。他自嘲 Earendil 可能是唯一没有「自动修 issue 机器人」的 harness 公司：「不是没试过软件工厂，是没成功。」

08｜关于烧钱，与最坏的结局

「如果按 API 价格付费，我根本不会怎么用 AI——那等于烧投资人的钱。」而他最怕的结局是：AI 像社交媒体一样，人人都在用、同时人人都在恨。

09｜欧洲为什么掉队

「欧洲的主题是保存过去，而不是启用未来。」根子上在于「欧洲不是一个国家」——27 套法律、27 种摩擦，有动力的人正在离开。

原访谈：[https://www.youtube.com/watch?v=SxuQs9GGYbk](https://www.youtube.com/watch?v=SxuQs9GGYbk)