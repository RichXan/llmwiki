---
title: "养成系私人助理 Hermes｜从入门到榨干"
source: "https://x.com/noahduck283/status/2099445686731427941"
author:
  - "[[@noahduck283]]"
published: 2026-09-14
created: 2026-09-15
description: "Grok Bot 如日中天，Hermes 还值得花时间配置吗？对我来说，值得我还是馋她的自由。它能接进微信、Telegram，模型由我选，资料由我管，做事方法不满意就打开改。比起直接用一套安排好的服务，我更想把现有的笔记、工具和习惯，接成一位长期搭档。这篇不赘述基础用法，只从私人..."
tags:
  - "clippings"
---
![Image](https://pbs.twimg.com/media/HSK2RUnaEAAJDsF?format=jpg&name=large)

Grok Bot 如日中天，Hermes 还值得花时间配置吗？对我来说，值得

我还是馋她的自由。它能接进微信、Telegram，模型由我选，资料由我管，做事方法不满意就打开改。比起直接用一套安排好的服务，我更想把现有的笔记、工具和习惯，接成一位长期搭档。

这篇不赘述基础用法，只从私人助理这个定位出发，由快速安装和最优设置开始，先带你把这套用法配起来：再用聊天管理资料，让固定搭档分工，把重复工作交给定时任务。最后配上 5 个私人助理向实用 Skill，借鉴海外玩家在学习、旅行、做饭等生活场景里的AI native用法。

# 目录

- 一、基础介绍与安装
- 二、最优设置
- 三、核心能力实战
- 四、私人助理进阶：5 个实用 Skill，5 位海外玩家的生活用法

# 一、基础介绍与安装

## 1.1 Hermes 是什么，适合拿来做什么

**Hermes 是 Nous Research 开源的个人 AI Agent，核心定位是能从做事过程中积累经验的长期助理。** 它运行在你的电脑或服务器上，接入模型后，可以查网页、改文件、运行程序，也能通过微信、Telegram 接任务、按时交付结果。

![Image](https://pbs.twimg.com/media/HSK0zW8bsAAgyyV?format=jpg&name=large)

它的“养成”有几件很具体的事值得讲。

**一、可以拿一整份资料，教它一套新本事。** /learn 接受网页、文档目录、PDF，也能学习刚刚完成的工作流程。遇到一本书或大批资料，它会按章节或主题提炼，做成带索引、按需读取的知识技能；同主题补进新材料，还能更新原来的技能。比如把自己的写作规范和参考资料交给它，以后处理相关任务时调用，不必每次重新贴一遍。[学习资料与技能](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills/#learning-a-skill-from-sources-learn)

**二、做完任务，还能回头修改自己的工作方法。** 内置后台复盘会尝试从你的纠正、成功步骤和踩过的坑里提取经验，更新记忆或技能。你还可以在桌面输入 /journey，打开学习记录的星图，查看积累了哪些内容，直接编辑或删除。助理学偏了，有地方能查、能改。[后台复盘与学习记录](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory/)

**三、没记进长期记忆的事，也能去旧聊天里找。** Hermes 会保存会话，支持检索实际消息，并继续翻看前后文。你问“上次为什么放弃那个方案”，它可以回到当时的对话找依据，减少你翻聊天记录、补背景的功夫。[旧会话检索](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory/#session-search)

**四、把任务交给其他 Agent 后，你还能接着聊。** 子任务可以在后台并行执行，完成后把结果送回原对话。需要复核时，输入 /review 就能派出独立审阅者，读取文件、调用工具检查刚才的成果；主助理收到意见后可以继续修改。查资料、整理和核查因此能分开安排。[后台协作与审阅](https://hermes-agent.nousresearch.com/docs/user-guide/features/delegation/)四、将任务交给其他 Agent 之后，你仍然可以继续进行对话。子任务可以在后台并行执行，完成后将结果返回到原始对话中。当需要复核时，输入/review 就可以派遣专门的审核人员，来读取文件、调用工具来检查刚才的成果；主助理收到意见后就可以继续进行修改。因此，资料收集、整理和核查等工作可以分开安排。后台协作与审核工作因此可以更加高效地进行。

## 1.2 比起 Grok Bot，Hermes 强在你能掌握得更多1.2 与 Grok Bot 相比，Hermes 的优势在于它能够让使用者掌控更多的功能。

Grok Bot 的省心在于云端电脑随时待命。Hermes 更适合我想要的这套玩法：**自己选模型，把助理接进常用聊天工具，连同积累一起迁走。**

![Image](https://pbs.twimg.com/media/HSK0zW5bUAAgR53?format=jpg&name=large)

资料核验：[Hermes 模型接入](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart/) · [角色导出与迁移](https://hermes-agent.nousresearch.com/docs/user-guide/profiles/#sharing-a-profile) · [Hermes MIT 许可](https://github.com/NousResearch/hermes-agent/blob/main/LICENSE) · [Grok Bot 设置](https://docs.x.ai/grok-bot/settings-and-notifications) · [Grok Bot 角色分享](https://docs.x.ai/grok-bot/faq)数据验证：Hermes 模型的接入 · 角色的导出与迁移 · Hermes MIT 许可协议 · Grok Bot 的设置 · Grok Bot 角色的共享

这对我最实际的好处是：**模型服务变了，原来的笔记、记忆和做事方法还能接着用。** 以后搬到常驻机器上，也能导出角色再导入，具体操作放在第三章。

喜欢 Grok 模型，也可以把它接给 Hermes 用。官方提供 xAI API 和 **xAI Grok OAuth** 两条路线，后者可接 SuperGrok / Premium+ 订阅；在 hermes model 中选择对应入口即可。[模型接入说明](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart/)

微信机器人私聊、Telegram 则把入口放到了聊天列表里。Telegram 支持文字、语音、图片和附件，也能接收定时任务结果，适合随手交资料、等它处理完再看。[Telegram](https://hermes-agent.nousresearch.com/docs/user-guide/messaging/telegram/) · [微信](https://hermes-agent.nousresearch.com/docs/user-guide/messaging/weixin/)

这套用法需要自己维护机器和连接，适合愿意花点时间，把现有资料库、模型账户和工具接起来的人。

## 1.3 安装与模型接入：各平台怎么选

**Mac、Windows、Linux 都可以用，本文只是用 Mac 截图演示。** 先按自己的设备选择入口：

![Image](https://pbs.twimg.com/media/HSK01jhaYAE_Nbd?format=jpg&name=large)

当前官方支持表不再支持 Intel Mac，老款 Mac 读者先看[平台说明](https://hermes-agent.nousresearch.com/docs/getting-started/platform-support/)，不要直接照搬 Apple 芯片路线。

桌面安装器会准备桌面应用和 hermes 命令，两者共用同一套账户与配置。安装结束后打开**新的**终端窗口，输入 hermes --version；能看到版本号，再继续接模型。

Linux / WSL2，以及桌面安装器失败的 Mac，在终端运行：

  
```bash
curl -fsSL https://hermes-agent.nousresearch.com/install.sh | bash
```

Windows 如果改用脚本安装，则在 **PowerShell** 运行下面这一条，别复制上面的 Bash 命令：

  
```powershell
iex (irm https://hermes-agent.nousresearch.com/install.ps1)
```

脚本安装完成后，想使用桌面界面再输入 hermes desktop。服务器只准备接消息入口的话，不必安装桌面。[安装说明](https://hermes-agent.nousresearch.com/docs/getting-started/installation/)

**模型接入优先复用已有账户。** 各平台都在终端输入：模型接入优先使用已有的账户。 各个平台都在终端输入：

  
```bash
hermes model
```

已有 ChatGPT / Codex 订阅，选择 **ChatGPT or Codex Subscription**；已有 Codex CLI 登录时选择导入，否则跟随向导在浏览器完成登录。接入其他服务，就选对应提供方，填写它要求的 Key 或服务地址。

不想用终端，也可以进桌面端 **设置 → 提供方 → 账号**，点击 **ChatGPT or Codex Subscription** 完成同一套浏览器授权。订阅登录走“账号”，不要误进旁边的“API 密钥”；后者会按 API 账户另外计费。

回到桌面 **设置 → 模型**，确认提供方及模型。这里只需要选一个现有账户可用、支持工具调用的模型；暂时沿用默认推理强度。开一条新对话，能收到回答就可以进入第二章。若提示未登录或模型不可用，回到 hermes model 修正；若找不到命令，先重新打开终端。[模型接入向导](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart/)

# 二、最优设置

我琢磨东西喜欢折腾最优配置，如果想快速使用，可以跳转第三章；

下面按**个人使用、处理资料和日常事务、以后接微信或 Telegram**来配：开启经验积累和长对话压缩，给文件修改留下撤回手段。

**第一次用，先配好 2.1 的目录和 2.2 的网页工具，存下一份资料。** 性格、记忆和长对话设置接着配，手机显示等接入时再调。

桌面配置前，先看设置页顶部的 **“应用于”**。第一次一律选 **default**，也就是平时点“新建会话”叫出的默认助理。第三章新建研究员后，再单独给研究员配置。

先记住三个位置，后面就不容易配错：

- **应用于：你正在改哪位助理。** 选错了，设置会跑到另一个角色身上。
- **窗口底部的项目：这次从哪个文件夹开始工作。** Hermes 读写的文件通常都在这里。
- **网关：真正运行 Hermes 的那台电脑。** 现在用自己的 Mac，就是本地网关；以后搬到旧电脑或服务器，再切远程网关。

设置改完后新建一条对话再测试。正文里的 hermes config set 是“修改设置”的终端命令，hermes config get 是“查看当前值”；只想用桌面界面的读者可以先跳过这些命令。

## 2.1 把知识库放在自己的目录里，再告诉它怎么整理

**推荐独立建一个 Hermes工作台，不要直接把整个电脑用户目录当工作区。** 在里面建三个文件夹：收件箱 放新材料，资料库 放确认保留的内容，成果 放简报、清单和整理结果。已有 Obsidian 或 Markdown 库，可以沿用原来的资料目录，不必迁移成 Hermes 专用格式。

进入 **设置 → 工作区 → 工作目录**，填入这个工作台的完整路径。Mac 在 Finder 选中文件夹，按 ⌥⌘C 复制路径；Windows 在资源管理器选中文件夹，右键“复制文件地址”（部分版本需按住 Shift）。粘贴进设置时，去掉外层引号。

![Image](https://pbs.twimg.com/media/HSK02-da0AA3u29?format=jpg&name=large)

图中的 . 表示沿用当前运行位置。想让每次新任务都落到同一处，就换成自己的路径；只处理资料时，“自动发现代码仓库”关掉，扫描根目录留空。已有项目会话仍可能使用它绑定的项目目录。

同页下面还有四项，先照着这样填：

  

| 页面选项 | 推荐值 | 它实际控制什么 |
| --- | --- | --- |
| 代码执行模式 | Project | 命令在当前项目文件夹里运行 |
| 持久化 Shell | 打开 | 前一条命令切换过的目录，下一条还能接着用 |
| 环境变量透传 | 留空 | 暂时不把电脑中的其他变量交给 Hermes |
| 文件读取上限 | 100000 | 一次最多读取多少字符；不是知识库总容量 |

文件太长时让 Hermes 分段读取，不必为了导入大资料就把最后一项调得很高。

改好后，新建对话，发送“告诉我你现在的工作目录”。它返回刚才的文件夹，就说明生效了。喜欢用终端的读者也可以输入下面两行；Windows 将示例路径换成自己的 C:/.../Hermes工作台：

  
```bash
hermes config set terminal.cwd "/你的完整路径/Hermes工作台"
hermes config get terminal.cwd
```

再规定资料怎么保存。这个要求写在工作台最外层的 .hermes.md 里，Hermes 每次进入这个文件夹都会先读它。

Mac 不方便直接在 Finder 新建以点开头的文件，可以打开终端，复制下面三行。第一行先进入工作台，第二行新建文件，第三行用系统文本编辑器打开：

  
```bash
cd "/你的完整路径/Hermes工作台"
touch .hermes.md
open -e .hermes.md
```

Windows 打开记事本，另存为 .hermes.md；“保存类型”选“所有文件”，避免被保存成 .hermes.md.txt。然后写入：

  
```markdown
# 资料管理约定
收到新材料，先放收件箱，保留原文、来源链接和收集日期。
随手记录先保留原话；只有明确要求整理时，才另写摘要或提纲。
整理到资料库时，保留出处，并把我的想法与原作者观点分开。
相同来源先查重；已有资料优先补充，不重复建立多个副本。
整理结果写入成果目录；修改原文前先说明准备改什么。
找不到依据时明确说未找到，不补造我的旧观点。
```

保存后新建会话，发送“复述这个目录的资料管理约定”。它能说出“收件箱、资料库、成果”三层规则，就说明文件放对了。如果目录里已经有一份 .hermes.md，直接在原文件末尾补充，不要新建第二份。

## 2.2 工具按职责开启，搜索和读网页分别配置

这项不在“设置”弹窗里。先关闭设置，回到 Hermes 主界面，在左侧点 **技能与工具**，再点页面顶部的 **工具集**，把“正在配置”选为 **Hermes (default)**。资料型助理建议开启：

这几个名字看起来很像，可以把 Hermes 想成一个刚入职的人：

  

| 名称 | 白话解释 |
| --- | --- |
| Skill | 操作说明书，告诉它一件事应该按什么步骤做 |
| 工具集 | 能力开关，决定它能不能读文件、搜网页、运行命令 |
| 工具与密钥 | 登录凭证存放处，例如把网页搜索服务的 Key 填在这里 |
| MCP | 外部服务接口，用来连接其他软件或数据 |
| 插件 | 能力安装包，一次可以带来 Skill、工具和 MCP |

**装了 Skill，不等于对应工具已经能用。** 就像给人一本“如何发邮件”的说明书，不代表他已经登录了邮箱。刚开始先开够用的工具集，遇到明确需求再装插件。

  

| 工具集 | 推荐用途 |
| --- | --- |
| File Operations、Terminal & Processes | 读写本地文件，调用 QMD、Blogwatcher 等已安装工具 |
| Web Search & Scraping | 找网页与提取原文 |
| Memory、Skills、Session Search | 保存记忆、调用工作方法、搜索旧会话 |
| Cron Jobs | 需要定时订阅或提醒时开启 |
| Browser Automation 等其他能力 | 只有网站需要登录或普通提取拿不到内容时，再配置浏览器路线 |

不要把 23 个工具集全部打开。默认助理保留上表这些，再按任务增加 **Vision、Task Planning、Task Delegation**；Computer Use、图片与视频生成、Spotify、Home Assistant、X Search 等用到再开。每位固定搭档单独配一遍，研究员不需要一整套做图、写代码和音乐工具。

**网页服务建议先用普通 Firecrawl，同时负责“找网页”和“读正文”。** Firecrawl 是独立的网页读取服务，Key 相当于它的登录凭证。点击 Web Search & Scraping 的名称，在右侧 Firecrawl 一行分别点 **“用于搜索”**、**“用于提取”**；已有 Key 就填对应字段。

![Image](https://pbs.twimg.com/media/HSK03IlbUAA-JBS?format=jpg&name=large)

同一提供方被选中后，会显示两种后端标记，对应按钮变灰。普通 Firecrawl、自建 Firecrawl、Nous Subscription 是三条接入路线，没有自建环境或 Nous 订阅就不要选后两项。

**偶尔体验先试免 Key，经常查资料就配自己的 Key。** 免 Key 会受公共服务限流和网络影响。获取 Key 的入口是 [Firecrawl 控制台](https://www.firecrawl.dev/)，填完再开新对话。终端用户运行 hermes tools，进入 **Web Search & Extract → Firecrawl** 完成同样配置。模型订阅不自动覆盖独立网页服务的用量。

“搜索近期发布”用搜索服务，“读这篇链接”用正文提取。换成只支持搜索的服务时，另外保留一个提取服务；配好后分别试一次搜索和读取。

网页必须登录时，先看内置路线：到 **设置 → Browser** 打开 **Use My Real Browser Profile**。Hermes 会复制当前 Chrome、Edge、Brave 或 Chromium 的活动配置到独立快照，在后台使用已有登录状态，不会直接占用正在浏览的配置目录；每次新建浏览器会话时重新同步。这个开关等于允许 Agent 以你的登录身份访问网站，只在确实需要的角色上开启。Windows 复制配置前还要彻底退出浏览器。

配好后，整理一份带出处的简报：

> 读取 [https://github.com/NousResearch/hermes-agent/releases/tag/v2026.9.7](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.9.7) ，整理三项普通使用者值得关注的变化，保留原始链接，保存到成果目录的“更新简报.md”。

右侧文件栏找到 成果/更新简报.md，双击并选择“预览”。也可以换成你本来就想收藏的文章。搜索限流时，先直接提供原文继续整理。

Skill 在 **技能与工具 → 技能** 中按角色管理。保留常用的，停用与角色职责无关的，减少相似技能之间的冲突。Skill 提供做事方法，还需要相应工具：邮件 Skill 要有邮件材料或邮箱连接，QMD 要有检索程序和索引，第四章分别讲怎么接。

## 2.3 性格自己写，记忆让它积累，但要看得见

**先分清三种“它知道的东西”：** SOUL.md 管它怎么说话、怎么做决定；记忆保存“你偏好短回答”这类长期习惯；文章、笔记和原始资料仍放在自己的资料库。以后回答方式不对就改 SOUL.md，它记错了就改记忆，要找原文就查资料库。

SOUL.md 不在普通设置页里。打开终端，输入 hermes config path，屏幕会返回一个以 config.yaml 结尾的位置。打开这个文件所在的文件夹，在旁边找到或新建 SOUL.md，补上例如：

  
```markdown
你是我的私人助理，回答先给判断和下一步，再补理由。
我只是随手记一件事时，简短确认；我要求分析时，再展开。
缺少会改变结论的信息才提问，不用每一步都向我索取确认。
发现我的判断有问题，直接指出依据，不为了顺着我而附和。
需要我选择时，优先给一个推荐，并说清取舍。
```

这里的 ~ 代表当前用户的个人文件夹。SOUL.md 默认在 Mac/Linux 的 ~/.hermes/，Windows 的 %LOCALAPPDATA%\\hermes\\；以命令实际返回的位置为准。保存后新建对话，让它“用两句话说明你的回答方式”，检查新性格是否生效。第三章的每个固定角色都可以有自己的 SOUL.md。[性格文件说明](https://hermes-agent.nousresearch.com/docs/user-guide/features/personality/)

接着进 **设置 → 记忆与上下文**：

![Image](https://pbs.twimg.com/media/HSK0357bEAAys9D?format=jpg&name=large)

  

| 设置 | 我的建议 | 为什么这样选 |
| --- | --- | --- |
| 持久记忆 / 用户画像 | 都开 | 前者保存环境与长期约定，后者保存你的稳定偏好 |
| 记忆预算 / 画像预算 | 2200 / 1375 字符 | 这些内容会随请求进入上下文；适合短而稳定的信息，不适合塞文档全文 |
| 记忆提供方 | 仅内置 | 先把记忆存在本机；有明确需要时再连接其他记忆服务 |
| 记忆写入审批 | 个人专用先关 | 保留自动积累的便利；若它反复记错或混入他人偏好，再打开逐条确认 |

记忆文件在同一配置目录下的 memories/MEMORY.md 和 memories/USER.md。可以直接查看；也可以直接说“展示你记住的关于我的偏好，把第二条改成……”。预算不够时先删过期内容，仍明显影响有用信息的保存，再小幅增加，别一开始扩成几万字。

逐条审批的开关在终端设置：

  
```bash
hermes config set memory.write_approval false
```

需要人工把关就把 false 改为 true。CLI 可当场询问；消息入口中待批内容需要用 /memory pending 查看，再用 /memory approve 编号 或 /memory reject 编号 处理。**开了审批却一直不处理，助理的记忆就会停在待确认状态。**

## 2.4 开启自动复盘，给长对话减负

“后台复盘”就是任务结束后，再让模型看一遍：这次有哪些偏好、成功步骤或错误值得留到下次。个人助理建议开启，先沿用正在聊天的主模型。桌面端到 **设置 → 模型 → 辅助任务模型 → 后台复盘** 配置；终端也可以输入：

  
```bash
hermes config set auxiliary.background_review.enabled true
hermes config set auxiliary.background_review.provider auto
hermes config unset auxiliary.background_review.model
```

自动复盘会增加模型用量。主要处理一次性任务、几乎不需要积累经验，或者额度吃紧时，把 enabled 改为 false，需要时用 /refine 手动复盘。已有便宜且可靠的模型服务，也可在 **设置 → 模型 → 辅助任务模型** 单独分配；先看实际用量，再决定要不要拆。

模型页还有三处容易误开：**上下文窗口保持 0**，让 Hermes 自动读取模型能记住多少内容；**备用模型**只在你已经接好第二家模型服务时添加，用来应对限流和故障；**Mixture of Agents** 可以理解成“多模型会诊”，它会先让几个模型分别回答，再让一个模型汇总，效果可能更稳，但调用次数和费用也会增加。它适合少量重要判断，不适合作为日常助理默认设置。

辅助任务不用都跟主聊天抢最强模型。压缩、标题和技能搜索可以交给便宜模型，/review 审查和主任务继续用更可靠的模型。

**同主模型的后台复盘会继承主任务的推理强度。** 想降低这部分用量，可以关闭自动复盘或另选辅助模型。[后台复盘说明](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory/)

再到 **设置 → 记忆与上下文**，向下滚动到压缩部分。“压缩”只会把较早的聊天整理成摘要，不会压缩或删除资料库里的文件。

![Image](https://pbs.twimg.com/media/HSK04QGboAANfFB?format=jpg&name=large)

  

| 选项 | 推荐值 | 取舍 |
| --- | --- | --- |
| 上下文引擎 / 自动压缩 | Compressor / 开 | 将较早的对话整理后继续使用，避免越聊越大 |
| 压缩阈值 | 0.5 | 用到模型上下文容量约一半时开始压缩，给后续材料和工具结果留余量 |
| 保护最近消息 | 20 | 保留近期修改来回，减少“刚指出的问题在压缩后丢了” |
| 压缩目标 | 先留 0.2 | 压缩后把旧聊天缩到较小体积，给后续对话腾出空间 |

频繁处理很长的逐字稿、且确实需要前后原话对照时，可以试着把阈值调到 0.7；代价是每轮携带更多内容。日常收资料与问答仍建议 0.5。合同数字、引文和正式决定应落进文件，不能只依赖压缩摘要。

**压缩摘要也会调用模型。** 已有主模型支持推理档位时，摘要这类辅助工作可以设成低档，主对话不变：

  
```bash
hermes config set auxiliary.compression.reasoning_effort low
```

模型不支持该档位时，沿用提供方默认值。

## 2.5 权限分三层，给资料修改留一条退路

**日常审批推荐 Smart，超时填 300 秒，命令白名单留空。** 入口在 **设置 → 安全**。审批就是 Hermes 准备执行删除、安装等高风险操作时，先停下来问你。

![Image](https://pbs.twimg.com/media/HSK040XasAA-uvz?format=jpg&name=large)

Smart 会评估命中危险规则的命令，风险不确定时询问；Manual 将这类命令交给你审批；Off 关闭这层审批。日常保留 Smart。

弹窗中，“仅此一次”适合临时动作，“本会话”只对当前会话放行，“始终允许”会形成长期规则。不要为了少点几次按钮，把宽泛命令加进白名单；已经误加的，可以回到这里删除。

**会反复改笔记或文档，我建议额外开启“文件检查点”。** 在同一安全页往下滚动，找到下图开关：

![Image](https://pbs.twimg.com/media/HSK05F7aUAAGfV3?format=jpg&name=large)

对应命令是 hermes config set checkpoints.enabled true。它会在支持的文件写入、修改和部分破坏性命令前保留检查点；代价是占用本地存储。只查资料、不改原文件的角色，可以保持关闭。

要撤回时，在交互式 CLI 中用 /rollback 查看编号，先用 /rollback diff 编号 看差异，再用 /rollback 编号 文件路径 恢复指定文件。它只能恢复本地文件。[恢复用法](https://hermes-agent.nousresearch.com/docs/user-guide/checkpoints-and-rollback/)

**第三层是执行环境，也就是命令到底在哪儿运行。** 到 **技能与工具 → 工具集 → Terminal & Processes**，处理自己电脑的文件时选 Local。它会继承当前电脑账户的文件权限；需要运行来路不明的脚本时，再使用 Docker 等隔离环境，并且只给它必要的文件夹。

无人值守时保留拒绝危险操作：

  
```bash
hermes config set approvals.cron_mode deny
hermes config set approvals.unattended_mode deny
```

“确认 MCP 重载”和“隐去密钥”保持开启；“允许私有 URL”保持关闭，确实要访问自建内网服务时再按服务需求配置。

## 2.6 把唤起、通知和常驻三件事配好

**先开快速输入。** 到 **设置 → 高级 → 快速输入**，打开开关。默认快捷键在 Mac 是 ⌘ + Shift + Space，Windows 是 Ctrl + Shift + Space。以后在浏览器、PDF 或笔记软件里按一下，就能唤出小输入框把任务交给 Hermes，不必先切回主窗口。

输入框里再记两个动作：输入 @ 添加文件、文件夹或网址；Hermes 正在执行时，Mac 按 ⌘ + Enter、Windows 按 Ctrl + Enter，可以把下一条消息排到当前任务之后。直接按 Enter，则会立刻把这条补充交给正在执行的任务。完整快捷键都能在 **设置 → 键盘快捷键** 里修改。

**通知只保留会改变下一步的事件。** 在 **设置 → 通知** 保留“需要批准、需要输入、本轮失败、额度提醒”。长任务经常放到后台，再保留“回复就绪”；若完成提示太多，关闭“后台任务完成”和提示音。桌面通知只在 Hermes 位于后台时出现，而且每台电脑分别保存。

觉得对话里工具日志太多，到 **设置 → 外观 → 工具调用显示** 选“产品”；需要排错或为教程截图时再切“技术”。同页打开“默认折叠推理过程”，内容仍保留，平时不会挤占阅读位置。

再到 **设置 → 对话 → 时区**，人在中国通常填 **Asia/Shanghai**；终端等价命令是 hermes config set timezone Asia/Shanghai。尤其是装在海外服务器上时，不要依赖服务器本地时区，否则“明天早上八点”可能按另一个时区执行。

需要运行长任务、定时任务或消息网关时，到 **设置 → 高级** 开启 **保持电脑唤醒**。它只能防止空闲休眠，不保证 Mac 合盖后继续运行。经常在研究员、核查员之间切换，可以把 **Warm Bot Backends** 留在 2—3 个；每多保留一个后台约多占 60 MB 内存，没必要把所有角色都常驻。

**网关可以理解成 Hermes 的后台主机。** 你的对话发给它，它负责调用模型、读写文件和执行定时任务。第一次使用选“本地”，让当前电脑承担这些工作。以后想让旧电脑或服务器全天待命，再进入 **设置 → 网关 → 通过 SSH 连接**；桌面端会自动建立加密连接，不需要把服务端口暴露到公网。

每台网关都有自己的聊天、消息入口和定时任务。把桌面端从 Mac 切到服务器，并不会自动把原来的任务搬过去。远程连接时，再打开“使用系统钥匙串加密已保存的机密”。

接好消息入口后，我会关掉逐条工具播报，保留结果和记忆更新。只用电脑的读者可以跳过下面这组消息显示设置。

以 Telegram 为例，终端输入：

  
```bash
hermes config set display.platforms.telegram.tool_progress off
hermes config set display.platforms.telegram.show_reasoning false
hermes config set display.platforms.telegram.interim_assistant_messages false
hermes config set display.platforms.telegram.memory_notifications verbose
```

微信把上述路径中的 telegram 换成 weixin。最后一项先用 verbose，是为了看清它到底记住或改进了什么；熟悉以后改为 on，只保留简短通知。想看长任务的阶段进度，把 interim\_assistant\_messages 恢复为 true 即可。

# 三、核心能力实战

## 3.1 养几个固定搭档，让查资料、写稿、核查接力

经常查资料，就养一个研究员；重要结论需要复核，再给它配一个核查员。职责和方法留在各自的角色里，下次直接找它。

我们先建一个研究员。展开左侧栏，进入 **BOTS**，点击标题旁的 **＋ → 新建机器人**，填写：

- **Name** 填 my-researcher：系统调用这个角色时使用的代号
- **Title** 填 研究员：左侧栏显示给你看的名字
- **Description** 填 查官方来源，保留链接，把更新写成普通人能用的简报：这个角色负责什么

![Image](https://pbs.twimg.com/media/HSK05puaoAEqYTv?format=jpg&name=large)

Name 不能和已有角色重复；不确定时照着上面的示例填即可。

展开 **高级 → General**，按下面填写。目的只有一个：复制 default 已经接好的账户和模型，不用再从头配置一次。

- Clone from profile 选 **default**：复制默认助理的基础设置。
- Provider 保持 **Inherit (launch profile)**，Model 留空：继续使用 default 的模型。
- **Share keys & accounts with the main profile** 保持勾选：继续使用已经登录的账户和 Key。
- Create empty 先不勾：第一次先从 default 复制，熟悉以后再从空白角色开始。
- SOUL.md 先留空：确实需要不同说话方式时再写。

![Image](https://pbs.twimg.com/media/HSK057RbgAAAiHK?format=jpg&name=large)

点击 **Create Bot**。左侧出现研究员后，先给能力做减法。克隆 default 只是为了复用账户和基础设置，不要把它携带的全部 Skill 都留下。到 **技能与工具 → 技能**，把“正在配置”切到研究员：保留 grounded-citations、blocked-page-recovery、pdf、rss-feeds 等研究能力，再按第四章加入 QMD、Blogwatcher；做图、写代码、音乐和邮箱 Skill 用不到就关。熟悉以后，新建窄角色可以勾 **Create empty**，从空白能力集开始添加。

到 **设置 → 高级 → 并行子智能体** 填 3。这是同时工作的上限，不是越大越聪明；普通订阅一次放出十个角色，更容易撞上并发限制，也会放大模型用量。

接着打开研究员的固定对话，让它改好我们刚才那份简报：

> 读取成果目录的“更新简报.md”，回查其中的 Hermes 官方发布链接。把每项改为“变化、用途、下一步”三句话；删掉与普通使用者无关的条目，修改原文件。

如果结果基本对，但你希望它以后都先讲用途、后放技术细节，就在同一个对话里继续输入：

> /learn 保存刚才的工具简报方法：开头最多三项，先讲是否需要升级、具体用途、下一步操作；技术细节后置，保留版本日期和出处。不要保存这次工具的版本号。

到 **技能与工具 → 技能**，切换到研究员，查看刚生成的方法。新建对话时仍选这个角色，换另一份材料，让它使用这份 Skill 处理。没有自动选中时，在任务里直接写出 Skill 名称。

要复核关键事实，按同样方法创建 my-checker，Description 写 打开原始来源，核对关键事实，只列影响结论的问题。研究员完成后在输入框输入 @ 选择核查员，让它检查同一份文件，再把问题交回研究员修改。两个角色使用同一工作目录，才能围绕同一份成果接力。[Bot 操作说明](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/website/docs/user-guide/bot-mode.md)

**养好以后，换机器也能带走。** 在原电脑终端导出研究员：

  
```bash
hermes profile export my-researcher -o my-researcher.tar.gz
```

把压缩包复制到新机器，在安装好的 Hermes 中导入：

  
```bash
hermes profile import ./my-researcher.tar.gz --name my-researcher
```

记忆、性格、Skill 和配置随角色导入。知识库目录另行同步，新机器接好模型账户和所需外部工具，再把工作目录指向同步后的资料。[导出与导入](https://hermes-agent.nousresearch.com/docs/user-guide/profiles/#sharing-a-profile)

## 3.2 多个任务持续跑，只汇总需要处理的变化

每天检查更新，最烦的是反复收到昨天已经看过的内容。给研究员安排定时任务时，把上次结果也交给它，这轮就能对照着找变化。

先把一次性任务做对，再给它安排重复执行。最直接的入口在主界面左侧 **定时任务**：Morning briefing、Weekly review、Topic news digest 等蓝图可以直接改；本文点击 **新建定时任务**。从 **BOTS → 研究员 → Routines** 进入的是同一类任务。

- 名称填 工具更新检查，频率先用 every 1h
- 执行角色选研究员，工作目录明确选择刚才的 Hermes工作台
- 打开 **continuity（连续记住上次结果）**，让本轮能参考自己的上次输出
- 投递目标先选“此桌面”，接好微信后再改到对应私聊
- 首次限制运行两轮，并确认时区、模型和下一次运行时间

工作目录不能省略：定时任务默认使用网关启动时所在的目录，不一定是你当前桌面会话的目录。它也归属于创建它的网关；远端网关停机，桌面开着也不会替它执行。

任务要求可以直接复制：

> 检查 [https://github.com/NousResearch/hermes-agent/releases](https://github.com/NousResearch/hermes-agent/releases) 是否有新的正式发布，对照成果/更新简报.md 和上次输出。发现新版本时更新简报，只汇报新增内容；没有变化时简短说明，读取失败时报告原因。

先立即运行一次，确认能读取发布页并找到已有简报；再跑第二次，检查是否重复报告同一版本。以后也可以把来源换成自己关注的博客或订阅页。

习惯终端的话，同一任务可以一次创建：

  
```bash
hermes -p my-researcher cron create "every 1h" \
  "检查 https://github.com/NousResearch/hermes-agent/releases 的新正式发布，对照成果/更新简报.md 和上次输出。发现新版本时更新简报，只汇报新增内容；没有变化时简短说明，读取失败时报告原因。" \
  --name "工具更新检查" \
  --workdir "/你的完整路径/Hermes工作台" \
  --continuity --repeat 2 --deliver local
```

创建后，用下面几行查看、试跑、暂停或恢复，把 任务ID 换成刚返回的 ID：

  
```bash
hermes -p my-researcher cron list
hermes -p my-researcher cron run 任务ID
hermes -p my-researcher cron pause 任务ID
hermes -p my-researcher cron resume 任务ID
```

桌面 **定时任务 → 运行记录** 可以查看每轮结果。continuity 会把上一次输出交给下一次任务，用来过滤已经汇报过的内容；每轮检查仍会调用模型。

同时盯几个来源时，让各个任务分别检查，再用一个汇总任务合并重复信息、标出更新时间，并单列读取失败的来源。[任务衔接文档](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/website/docs/user-guide/features/cron.md#chaining-jobs-with-context_from)

## 3.3 微信随手记，电脑接着找资料、做整理

**这一节受到金尘马的**[微信随记文章](https://x.com/jinchenma_ai/status/2097715636172665017)**启发。** 他把微信接到专用记录 Agent，让发过去的文字原样进入 Obsidian。我很喜欢这个出发点：有个念头，先留下来，整理可以晚一点。

这里继续用刚建好的研究员，在同一个聊天框里完成三件事：**记一下、找一下、整理一下。**

**先给研究员补三条工作约定。** 在电脑上打开 my-researcher 的对话，发送下面这段，让它把规则追加到工作台的 .hermes.md：

  
```text
请保留现有约定，补充以下聊天用法：
“记一下：”后面的内容存入收件箱，每条新建一份 Markdown；正文保留我的原话，日期和标题单独放，保存后回复文件路径。
“找一下：”表示搜索收件箱和资料库，给我匹配的原文片段与文件路径；没有匹配就说明没找到。
“整理一下：”表示按这次要求加工指定材料，成品另存成果目录，附上用到的原笔记路径。
这三个短语是任务标记，不写进笔记正文。
```

这些任务标记可以换成你习惯的词。原话留在收件箱，清单或提纲另存，需要时能回看当时的想法。

**把微信接到这位研究员。** 在运行 Hermes 的电脑上打开终端，将路径换成自己的工作台，依次输入：

  
```bash
hermes -p my-researcher config set terminal.cwd "/你的完整路径/Hermes工作台"
hermes -p my-researcher gateway setup
```

向导里选 **Weixin**，用手机微信扫描终端显示的二维码，再在手机上确认绑定。完成后打开对应机器人的私聊。这里的 -p my-researcher 指定接收消息的角色；以后查资料和改文件，都由它处理。

这里连接的是腾讯 iLink Bot 私聊身份，不是把个人微信交给 Hermes 操作。普通微信群通常不能邀请这个 Bot，也不会向它投递群消息；先把它当成自己的专用私聊入口。终端若没画出二维码而只给出一个临时链接，直接在电脑浏览器打开该链接再扫码即可。

扫码结束后，在桌面进入 **消息平台**，顶部选刚创建的研究员，再选 **Weixin / WeChat (Personal)**。看到 account ID、token 和 API 地址都显示“已保存”，打开底部开关并点击提示中的 **重启网关**。图中演示角色名是 researcher，正文中的 my-researcher 操作相同。

![Image](https://pbs.twimg.com/media/HSK06IaaEAAXrdv?format=jpg&name=large)

如果常常连续发几条独立随记，再设这一项：

  
```bash
hermes -p my-researcher config set platforms.weixin.extra.text_batch_delay_seconds 0
```

默认会等约 3 秒，把快速连发的文字合并处理；设为 0 后逐条交给助理，便于按刚才的约定分开保存。习惯分几条消息补充同一个问题，就保留默认值。

向导最后会询问是否立刻启动 Gateway，以及是否安装开机自动启动服务。个人电脑长期作为助理主机，两个问题都选 Y；这样终端可以关闭，Gateway 会在登录后启动，异常退出也会自动重启。临时试用或不希望长期驻留，跳过服务安装，改用 hermes -p my-researcher gateway run 前台运行。电脑仍需保持联网和唤醒。[微信接入与设置](https://hermes-agent.nousresearch.com/docs/user-guide/messaging/weixin/)

接好后，在微信发一条随记：

> 记一下：下次旅行想留半天逛旧书店，别把每天排得太满。

第一次私聊时，Bot 可能先返回一个 pairing code，而不执行任务。在运行 Hermes 的电脑上复制它给出的命令；如果正文里的角色名不是默认配置，要补上 -p my-researcher：

  
```bash
hermes -p my-researcher pairing approve weixin 你的配对码
```

批准后把刚才的“记一下”重新发送一次，以后这个微信用户会被自动识别。正确时它会回复保存路径；打开该路径，检查原话是否出现在 收件箱。已有 Obsidian 的读者，把工作台放在自己的笔记库内，就能直接在库里看到文件。Hermes 在另一台机器上时，需要让两台机器同步这个目录，沿用已有同步工具即可。

过几天只记得大意，也可以问：

> 找一下：我之前对旅行节奏有什么要求？把原话和笔记位置给我。

准备做行程时，再发：

> 整理一下：根据刚找到的旅行随记，列一份选行程时要遵守的要求，保存到成果/旅行要求.md。只整理我写过的内容，附上原笔记路径。

我自己的工作流还会再分一层：文章和链接先提取正文，留在 Clippings 原文库；随手记保留原话，落进 Inbox；选题直接进灵感库。只有我确认值得长期吸收的内容，才进入带出处的 Wiki。真正准备创作时，再从知识库选回灵感库，确认立项。

![Image](https://pbs.twimg.com/media/HSK06QwaIAASb4T?format=jpg&name=large)

最后也可以直接让它把 成果/旅行要求.md 发回微信。写文章、准备学习计划、整理购买意向，都能沿用这三个动作。资料多到普通文件搜索费力时，再接第四章的 QMD。

Telegram 可以使用同一套文件约定；在向导里改选 Telegram，按[官方向导](https://hermes-agent.nousresearch.com/docs/user-guide/messaging/telegram/)配置 Bot Token 和允许调用的用户。

# 四、私人助理进阶：5 个实用 Skill，5 位海外玩家的生活用法

## 4.1 给私人助理配齐的 5 个 Skill，按需选用

按自己最常遇到的麻烦挑 Skill。经常找不到以前为什么做了某个决定，就先装资料检索；每天被邮件和承诺追着跑，就先装沟通与周复盘。

![Image](https://pbs.twimg.com/media/HSK06gCbwAAyCsu?format=jpg&name=large)

官方 Skill 的统一入口是 **技能与工具 → 技能**。搜索名称，点击 **Add to this Agent**，装到准备长期使用它的 Bot。第一次接外部工具时，直接让 Hermes 读取 Skill 并一步一步带你完成，比自己先啃完整配置文档省力。[技能安装说明](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/website/docs/user-guide/features/skills.md#skills-hub)

## OpenCLI 让助理去你已经登录的网站找真实反馈

想知道一个工具值不值得试，可以让 Hermes 去找具体使用反馈和原帖。OpenCLI 能连接你已登录的 Chrome 或 Chromium，省去来回翻网页、复制材料的功夫。

在终端运行：

  
```bash
hermes skills install https://github.com/jackwener/OpenCLI/blob/main/skills/opencli-browser/SKILL.md
```

安装完成后，对 Hermes 说：

> 读取 opencli-browser 的 Skill 说明 带我完成 OpenCLI 和 Browser Bridge 的连接 每完成一步再继续 最后只读取当前网页标题验证连接 不发布任何内容

能读出当前页面的标题后，再让它找反馈：

> 使用 opencli-browser，从这个工具的相关讨论中找三条具体使用反馈。保留原帖链接、日期、对应版本和原话依据，说明哪些是个人体验。先只读取，不发帖。

如果你现有的浏览器工具已经能稳定完成这件事，OpenCLI 可以后装。[Skill 源文件与配置步骤](https://github.com/jackwener/OpenCLI/blob/main/skills/opencli-browser/SKILL.md)

## QMD 让它先翻旧资料再给新建议

工具更新后，可以先翻出当初放弃它的原因。QMD 从文章、笔记和会议记录里找回相关原文，交给 Hermes 对照，判断这次有没有解决那个问题。

在技能中心搜索 qmd 并安装，然后发：

> 读取 qmd 的 Skill 说明 带我把这个资料夹加入检索 先完成一次关键词搜索 找到原文件和具体段落后再继续

第一次只给它一个小资料夹，确认真的能找回一段旧依据，再逐步增加资料。接好后可以直接问：

> 使用 qmd，在这个资料夹里找出我上次没有采用该工具的原因。返回原文件和相关段落，再和这次更新对照。找不到旧依据就直说，不要替我补一个理由。

[Hermes QMD 技能](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/optional-skills/research/qmd/SKILL.md)

## Blogwatcher 让它只告诉你新来的内容

Blogwatcher 保存订阅和已读状态。每天查博客与更新页时，Hermes 可以先处理新文章，不用你挨个辨认哪些已经看过。

在技能中心搜索 blogwatcher 并安装，然后说：

> 读取 blogwatcher 的 Skill 说明 带我安装当前使用的 blogwatcher-cli 再添加这两个订阅源 完成第一次扫描后停下来给我看结果

第一次只加两个你真的会看的 RSS 或 Atom 订阅。确认能看到文章后，再发：

> 使用 blogwatcher 管理这两个订阅源。列出新文章，附标题、日期与原始链接。我确认读完某篇后再标记已读；下一轮优先处理尚未读过的内容。

订阅和已读状态用顺后，再接第三章的定时任务。[Skill 源文件](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/optional-skills/research/blogwatcher/SKILL.md)

## Email Inbox Triage 帮你找回邮件里还没结束的事

一封邮件显示已读，不代表事情已经结束。你可能答应补一个附件，也可能还在等对方回复。这个 Skill 会沿完整邮件线程找出谁该行动、谁在等待，并先准备回复草稿。[Skill 源文件](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/skills/email/email-inbox-triage/SKILL.md)

它已经内置在 Hermes 中。在技能页搜索 email-inbox-triage 并打开。第一次先别交出整个邮箱，只提供三到五条完整邮件往来，然后发：

> 使用 email-inbox-triage，检查这些邮件线程。列出我还没回答的问题、已经答应但没完成的事，以及正在等对方的事。每项附对应原句和期限。需要回复的先写草稿，不发送、不删除邮件。

先人工核对这几条有没有判断错。靠谱以后，再决定是否给它接入邮箱，先保留只读和草稿权限。

## Weekly Review Planning 把散落一周的承诺收回来

这个 Skill 会对照一周的记录，找出停滞项目、答应过却没做的事、正在等的回复，以及下周排不下的计划。[Skill 源文件](https://github.com/NousResearch/hermes-agent/blob/v2026.9.7/skills/productivity/weekly-review-planning/SKILL.md)

它已内置。在技能页搜索 weekly-review-planning 并打开，再给它一个项目的任务记录、过去一周的日历和下周安排。没有连接账户时，直接导出或复制这些材料也能先跑一轮：

> 使用 weekly-review-planning，根据这些记录做一次周复盘。找出停滞事项、我答应过的事、等别人回复的事，并给出原始依据。结合下周已有日程，选出三项最值得完成的结果，说明哪些顺延。先给建议，不改日历和任务。

核对它找出的承诺，再看建议有没有避开已经占用的时间。判断可靠后，把它安排成每周固定任务。

第三章用微信存下的随记，也可以一起交给周复盘。让它把“随口想到的点子”和“已经答应要做的事”分开，只有后者进入待办；一句“以后想学摄影”，不该自动变成下周必须完成的任务。

## 4.2 把 Hermes 用进生活的 5 个方面

下面五位玩家的公开分享，可以借用到学习、旅行、家庭日程、菜单和票据管理里。

![Image](https://pbs.twimg.com/media/HSK07GNaMAA6rx4?format=jpg&name=large)

## Gordon Guocheng Qian 让学习从上次卡住的地方继续

Gordon 用 Hermes 回顾实际工作记录，通过周总结接续进度。学外语、摄影或剪辑也可以借用这个方法：每次结束时记下做会了什么、卡在哪里、下次先练什么，下次打开记录就知道从哪里继续。[原文](https://guochengqian.github.io/blog/hermes-agent/)

每次学习结束时发：

> 根据今天的笔记，记下我已经做会的部分、还解释不清的问题，以及下次先练什么。下次先从未解决的问题接着来。

把当天笔记、练习结果或一段语音转写一起给它。下次从这份记录继续。

## Brendan Tack 让旅行计划跟着每次变化一起更新

Brendan 把研究、项目简报、任务和成果放在一起，让后续决定落实到同一个项目里。这种做法也适合旅行：同行人不想早起、日期改了、酒店还没确认，都可以让助理据此调整行程、待办和预订记录。[原文](https://brendantack.com/blog/how-i-use-hermes-to-run-my-work)

> 出发日期改到下周。请更新当前行程和相关待办，并列出需要重新确认的预订。只有我提供的预订凭据能证明已经订好，不要把候选方案当成订单。

如果你经常等特定日期或积分价格，也可以让它只在满足条件时提醒。社区用户 julp 就分享过反复检查积分机票、符合条件才通知的用法。[补充来源](https://www.reddit.com/r/hermesagent/comments/1uwbeql/hermes_use_case_youre_most_proud_of/)

## Molly Lazarus 让日历记住活动之前还要准备什么

日历里记着活动日期，提前买礼物、交材料、准备衣服却容易漏。Molly 会把家庭聊天中的邀请截图和学校邮件转给 Hermes，让它记下日期，也安排提前准备的事项。[本人分享](https://www.linkedin.com/pulse/how-i-built-ai-assistant-our-family-molly-lazarus-snboc)

> 这是我准备参加的活动。请从通知里提取时间地点，列出明确需要准备的东西，并区分活动当天的提醒和必须提前完成的事情。原文没有写清的部分先指出来。

她还给助理安排了独立收件地址，只转发需要处理的邮件。你可以用同样的办法限定它收到哪些材料，不必一开始接入整个邮箱。

## Dave 让下一周菜单真的吸收这周的反馈

Dave 的使用记录里，每周选菜会继续参考之前的反馈。味道怎么样、做起来麻不麻烦、还想不想再吃，都会影响后面的建议。[博客记录](https://www.azathought.com/Blog-TAKEOVER/)

吃完以后告诉它：

> 这道菜好吃，但我工作日晚饭不想花这么久。保留它，周末再安排。下周工作日先选准备时间短的菜。

再把菜单接到购物清单：你告诉它家里已有的食材，家人补充缺的东西，它只整理真正需要买的部分。菜单变化以后，采购清单也会跟着更新。这是本文把 Dave 与 Molly 两种方法组合起来的用法。

## himore 让票据拍完就归档 月底直接出报销草稿

himore 会把照片、PDF、邮件和附件发给归档助理，存入 Obsidian 并返回位置；票据则交给另一个 Bot 记录，月底再生成公司报销表草稿。[原帖与追问](https://www.reddit.com/r/hermesagent/comments/1usj9yh/what_have_you_done_with_hermes_agent_this_week/)

票据平时拍下归档，月底就能据此整理报销草稿；保修邮件和购买凭据也有固定去处。

第一次拿三到五张票据和一份报销表副本试。让 Hermes 从原图生成明细并汇总，再随机找回一张原件核对。看不清的金额留给你确认，不要让它为了填满表格自动猜。

![Image](https://pbs.twimg.com/media/HSK0_JUbAAA3sLA?format=jpg&name=large)

工具会更新，模型也会换。只要资料、偏好和做事方法还在自己手里，每一次纠正就能让下一次少讲一句、少返工一步。

Hermes 的“养成感”就在这里：它越来越懂你，也始终是你能看见、能修改、能带走的长期搭档。

**我是诺鸭船长，带你在信息的海洋里寻找陆地～**