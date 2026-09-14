---
title: "写作指南：让 AI 写作无限接近你的真实文风"
source: "https://x.com/SenMufs/status/2099030779141783567"
author:
  - "[[@SenMufs]]"
published: 2026-09-13
created: 2026-09-14
description: "如果你用AI写过文章，你一定有过这样的感叹：写的压根不像我写的东西。翻译成大白话就是：没人味！以前我们解决这个问题靠的是提示词加上一大堆去Ai味的Skill，提示词写一句：不要有AI味、写的口语一点、不要太正式，解决不了任何问题。让AI写东西不带Ai味，好比嫖完劝别人从良。Ai写..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HSE83deawAAtgca?format=jpg&name=large)

如果你用AI写过文章，你一定有过这样的感叹：

写的压根不像我写的东西。

翻译成大白话就是：没人味！

以前我们解决这个问题靠的是提示词加上一大堆去Ai味的Skill，

提示词写一句：不要有AI味、写的口语一点、不要太正式，解决不了任何问题。

让AI写东西不带Ai味，好比嫖完劝别人从良。

Ai写完自己再改，工作量堪比重写一篇！

去AI味的skill可能有用，但还是解决不了最终问题：不像我写的。

这篇文章给大家一个新思路，逻辑简单，操作方便，立马可以上手，也不靠任何skill，但这可能是目前解决这个问题最有效的方法！

直接进入正题！

这套方案的核心就是：ChatGPT 的 Writing Style+Google Drive，打造一个完美写作工作流闭环。

内容主要有以下几个方面：

1、什么是writing Style、如何设置、如何使用。 2、writing Style如何和项目层配合。 3、Google Drive 如何配置。 3、writing Style如何和Google Drive配合，并形成写作风格库工作流的完美闭环。

## 一、什么是 Writing Style

Writing Style，不是让你重新再写一版更长的文风规范。

也不是让你每次写文章前都重复：写得口语一点、别太正式。

Writing Style，是一个可以自动整理、归纳你的写作风格并不断更新的机制，它可以连接 Gmail、Google Drive、Slack、SharePoint，然后参考你过去写过的邮件、消息和文章，从里面提取写作习惯、常用措辞、句式、结尾习惯、大小写习惯等特征，建立你的个人写作风格信息，在后续的写作任务中参考连接应用中的写作样本，并在之后帮你写消息、文档时自动模仿你的表达方式。

总结一下：

**Writing Style=自动维护的个人 Style Guide + 持续参考你的真实写作样本**

为什么有用？

以前让 AI 学自己，是自己写提示词：写得像我！那什么是像你？你的写作风格、习惯到底是什么？以前Ai靠猜，猜的好不好全凭运气，现在靠模仿靠拆解，范本就是你的真实产出，一切都有迹可循。

从你口述自己像谁，变成模型去看你已经写过的真实输出，

一个是时好时坏运气游戏，一个是有参考的真实模板，

提示词解决不了的问题，直接丢模版，效果往往意想不到。

打开这个功能也很简单：

打开Chat GPT 网页版—设置—个性化—writing style （写作风格）—开始设置—在数据来源里选择 Google Drive

![Image](https://pbs.twimg.com/media/HSE-NkXbYAAO6gn?format=jpg&name=large)

打开之后，在Chat GPT中连接Google Drive插件

![Image](https://pbs.twimg.com/media/HSE-TYlaMAETm9W?format=jpg&name=large)

## 二、Google Drive

说完Writing Style，在来说说 Google Drive

Google Drive就是谷歌云端硬盘，普通个人 Google 账号默认有 15 GB 免费存储空间。你可以把 PDF、图片、视频、Word、Excel、代码文件等放进去，文件保存在 Google 云端，在这套工作流当中，它充当着你的长期资料仓库的作用，用来保存你的文章、笔记、随笔，或者其它任何你想用来当模板的内容。这就是以后AI写文章时最直接的样本源。

你可以在里面建一个文件夹，结构参考如下：

```text
Eian Writing Corpus
├── 01 Long Form
├── 02 Short Posts
└── 03 About Me
```

设置路径为：打开Google Drive —我的云端硬盘—创建总文件夹—进入总文件夹在建3个子文件夹

![Image](https://pbs.twimg.com/media/HSE-ttsbQAAoUP8?format=jpg&name=large)

这 3 个文件夹分别放什么？

01 Long Form；放你已经写完的长文章。

02 short posts：放短一点的文字，例如你的随记、摘录、你随手写下的文字！

03 About Me：放描述你自己的资料，例如：个人简介、经历、常写的话题、不喜欢的表达等等

设置好这些，就可以逐渐往里面放东西，把自己的模版库建起来，素材越多，Chat GPT参考的素材越多，写的东西也越像你。

到这里其实这套工作流己经闭环了！

Chat GPT的Writing Style功能以Google Drive为数据来源总结我们的写作风格，我们把Google Drive打造成个人文本库。

但这样有一个问题，每写好一篇文章，就往里面放一次，太繁琐、效率太低，Agent时代讲究效率，这是绝不能容忍的！

所以更完美的方案是，建立一套机制！让一切真正闭环。

## 三、writing Style和项目层配合

这就需要在chat gpt链接上Google Drive插件发挥作用，Chat GPT可以通过连接的 Google Drive 插件，访问你授权范围内的 Drive 内容。

它可以直接：查看 Drive 里的文件和文件夹、搜索文件、读取 Google Docs / Sheets / Slides、以及后续在你明确要求时创建、整理或修改内容。

也就是是你对云盘的一切管理都可以在Chat gpt里完成，一句话的事儿！

然后这套工作流的就变成了这样：

**在Google Drive打造个人文本库——Chat GPT的Writing Style功能以Google Drive为数据来源总结我们的写作风格———将风格应用在下一次写作中———简单修改文章———文章定稿———Chat GPT自动把文章推送保存到Google Drive。**

![Image](https://pbs.twimg.com/media/HSFANIjaIAA7HwQ?format=jpg&name=large)

完美闭环！

而最后一步甚至不用你每次都说，你只需要在你的写作项目中，添加这样一段指令：

```text
当我明确表示某篇内容“定稿”“最终版”或要求“归档”时，将最终确认版本自动保存到 Google Drive 的 EWriting Corpus。根据内容类型放入 01 Long Form、02 Short Posts、03 About Me。只保存用户最终确认版本，不保存初稿、修改过程或参考资料。Google Docs 标题使用作品最终标题；如果短帖没有标题，则根据内容生成一个简短、便于检索的文件名。保存后确认文件已创建并位于正确目录。
```

当我明确表示某篇内容“定稿”“最终版”或要求“归档”时，将最终确认版本自动保存到 Google Drive 的 EWriting Corpus。根据内容类型放入 01 Long Form、02 Short Posts、03 About Me。只保存用户最终确认版本，不保存初稿、修改过程或参考资料。Google Docs 标题使用作品最终标题；如果短帖没有标题，则根据内容生成一个简短、便于检索的文件名。保存后确认文件已创建并位于正确目录。

全部搭好之后：以后写文章你可以用下面这条指令：

```text
写一篇****长文。
主题：【填写】
我真正想表达的核心：【填写】
必须包含的信息：【填写】
这次特殊要求：【没有就不写】
用我的writing style和 Writing Corpus，不要照抄旧文章。先帮我把文章逻辑和核心观点梳理清楚，再开始写。
```

写到这里，这套方法其实已经很清楚了。

先让 Writing Style 知道你平时是怎么写的。

再把 Google Drive 变成你自己的真实写作样本库。

以后每写完一篇满意的文章，就继续把它放回这个库里。

下一次写作时，AI 参考的就不再是一堆你临时写出来的“像我一点”“口语一点”“少点 AI 味”的提示词。

它不要求你先总结出一套完美的个人文风，再写成几十条提示词教给 AI。

而是反过来：直接以你为参考。

你写得越多，这个库就越完整，而这个库越完整，AI 对你的理解也就越有依据。

**你的文章、你的句子、你的表达习惯，本身就是最好的 Prompt。**