---
title: "养成系私人助理 Hermes｜从入门到榨干"
type: source
aliases:
  - "Hermes 私人助理养成"
  - "从入门到榨干"
tags:
  - source
  - article
  - Agent
  - Hermes
  - 教程
sources:
  - "[[raw/articles/养成系私人助理 Hermes｜从入门到榨干]]"
created: 2026-09-15
updated: 2026-09-15
---

# 来源摘要：养成系私人助理 Hermes｜从入门到榨干

## 摘要

本文作者（X：[@noahduck283](https://x.com/noahduck283)，自称"诺鸭船长"）给出把 [[hermes|Hermes Agent]] 当**私人助理**养的完整实操手册：从安装、最优设置、核心能力实战，到 5 个私人助理向 Skill 与 5 位海外玩家的生活用法。开篇即给出定位选择——"**Grok Bot 如日中天，Hermes 还值得花时间配置吗？对我来说，值得**，我还是馋她的自由"，即**自己选模型、把助理接进常用聊天工具、连同积累一起迁走**。

本文是 [[hermes]] 实体页的第一份**实操级来源**，与 [[agent自动化获客完整指南]]（仅提及 hermes 作为定时任务执行器）互补：前者讲"为什么用它做获客"，本文讲"**怎么把它当一个长期搭档养**"。

## 元信息

- **作者**：[@noahduck283](https://x.com/noahduck283)（自称"诺鸭船长"，身份待核实）
- **发布日期**：2026-09-14
- **原始链接**：https://x.com/noahduck283/status/2099445686731427941
- **原始文件**：`[[raw/articles/养成系私人助理 Hermes｜从入门到榨干]]`
- **入库日期**：2026-09-15
- **首次维护说明**：本批入库时该文正文中多处出现**中英文重复段落**（如第 1.1 节第四条、第 1.2 节标题、第 2.x 节末尾），疑为原文排版/机翻叠加所致，**本页保留原意、未逐字照抄重复部分**，已在「待核实」标注。

## 核心内容

### 1. 基础介绍与安装

**Hermes 是什么**：Nous Research 开源的**个人 AI Agent**，核心定位是**能从做事过程中积累经验的长期助理**。运行在自己的电脑或服务器上，接入模型后可查网页、改文件、运行程序，也能通过微信、Telegram 接任务并按时交付。

**四件"养成"能力**（作者列举 + 官方文档链接）：

| 能力 | 说明 | 命令/入口 |
| --- | --- | --- |
| **拿一整份资料教它新本事** | `/learn` 接受网页、文档目录、PDF，也能学习刚完成的工作流；按章节/主题提炼成**带索引、按需读取**的知识技能；同主题补新材料还能更新原技能 | `/learn` |
| **做完任务回头改自己的工作方法** | 内置后台复盘，从纠正、成功步骤、踩过的坑中提取经验，更新记忆或技能 | `/journey` 打开学习记录星图，可直接编辑或删除 |
| **旧聊天里找没记进长期记忆的事** | 保存会话、支持检索实际消息并翻看前后文 | 会话检索 |
| **把任务交给其他 Agent 后仍能接着聊** | 子任务后台并行执行，结果送回原对话；`/review` 派独立审阅者读文件、调工具检查成果 | `/review` |

**相比 Grok Bot 的差异**（作者视角）：

- Grok Bot 的优势是"**省心**"——云端电脑随时待命；
- Hermes 的优势是"**你能掌握得更多**"——自己选模型、接进常用聊天工具、**连同积累一起迁走**；
- 最实际的好处：**模型服务变了，原来的笔记、记忆和做事方法还能接着用**；
- **想吃 Grok 模型也可以接给 Hermes**：官方提供 **xAI API** 与 **xAI Grok OAuth** 两条路线，后者可接 **SuperGrok / Premium+ 订阅**，在 `hermes model` 中选择对应入口。

**消息入口**：Telegram 支持文字、语音、图片和附件，也能接收定时任务结果；**微信（iLink Bot）**私聊入口。

**安装**：

| 平台 | 方式 |
| --- | --- |
| Mac / Windows / Linux | 桌面安装器（准备桌面应用和 `hermes` 命令，两者共用同一套账户与配置）→ 打开**新的**终端窗口，`hermes --version` 验证 |
| Linux / WSL2，或桌面安装器失败的 Mac | `curl -fsSL https://hermes-agent.nousresearch.com/install.sh \| bash` |
| Windows（脚本安装） | PowerShell：`iex (irm https://hermes-agent.nousresearch.com/install.ps1)`（**不要复制上一条 Bash 命令**） |
| 服务器（只要消息入口） | 不必安装桌面；想用桌面界面再 `hermes desktop` |

⚠️ **平台支持变化**：作者明确指出**当前官方支持表不再支持 Intel Mac**，老款 Mac 读者先看平台说明。

**模型接入**：终端输入 `hermes model`，优先复用已有账户——已有 ChatGPT / Codex 订阅选 **ChatGPT or Codex Subscription**。桌面端走 **设置 → 提供方 → 账号**。作者提醒：**订阅登录走"账号"，不要误进旁边的"API 密钥"**（后者按 API 账户另外计费）。

### 2. 最优设置（作者的核心贡献）

**三个先记住的位置**：

| 概念 | 含义 |
| --- | --- |
| **应用于** | 你正在改哪位助理（选错会跑到另一个角色身上）；第一次一律选 **default** |
| **窗口底部的项目** | 这次从哪个文件夹开始工作（Hermes 读写的文件通常在这里） |
| **网关** | 真正运行 Hermes 的那台电脑（本地 Mac = 本地网关；搬到旧电脑/服务器后切远程网关） |

#### 2.1 知识库目录结构

推荐**独立建一个 `Hermes工作台`**，不要直接把整个电脑用户目录当工作区：

```text
Hermes工作台
├── 收件箱    # 放新材料
├── 资料库    # 放确认保留的内容
└── 成果      # 放简报、清单和整理结果
```

**已有 Obsidian 或 Markdown 库，可以沿用原来的资料目录，不必迁移成 Hermes 专用格式**（与作者自身 [[obsidian|Obsidian]] 工作流一致）。

工作目录设置（**设置 → 工作区 → 工作目录**）与配套四项推荐值：

| 页面选项 | 推荐值 | 实际控制什么 |
| --- | --- | --- |
| 代码执行模式 | Project | 命令在当前项目文件夹里运行 |
| 持久化 Shell | 打开 | 前一条命令切换过的目录，下一条还能接着用 |
| 环境变量透传 | 留空 | 暂时不把电脑中其他变量交给 Hermes |
| 文件读取上限 | 100000 | 一次最多读取多少字符；**不是知识库总容量** |

**资料管理约定写在 `.hermes.md`**（工作台最外层，Hermes 每次进入该文件夹都会先读）：

```markdown
# 资料管理约定
收到新材料，先放收件箱，保留原文、来源链接和收集日期。
随手记录先保留原话；只有明确要求整理时，才另写摘要或提纲。
整理到资料库时，保留出处，并把我的想法与原作者观点分开。
相同来源先查重；已有资料优先补充，不重复建立多个副本。
整理结果写入成果目录；修改原文前先说明准备改什么。
找不到依据时明确说未找到，不补造我的旧观点。
```

> 🔗 这套约定与本库 [[AGENTS|AGENTS.md]] 的核心规则**高度同构**（收件箱≈`raw/`、资料库≈`wiki/`、成果≈产出层；"保留出处""我的想法与原作者观点分开""不重复建副本""找不到依据不补造"）。**但它是给 Hermes 用的约定示例，不是本库规则的来源。**

#### 2.2 工具按职责开启

**五个易混概念**（作者给出"刚入职的人"比喻）：

| 名称 | 白话解释 |
| --- | --- |
| **Skill** | 操作说明书，告诉它一件事应该按什么步骤做 |
| **工具集** | 能力开关，决定它能不能读文件、搜网页、运行命令 |
| **工具与密钥** | 登录凭证存放处（如搜索服务的 Key） |
| **MCP** | 外部服务接口，用来连接其他软件或数据 |
| **插件** | 能力安装包，一次可以带来 Skill、工具和 MCP |

> ⚠️ **重要区分**：**装了 Skill ≠ 对应工具已经能用**，"就像给人一本'如何发邮件'的说明书，不代表他已经登录了邮箱"。

推荐开启的工具集（**不要 23 个全开**）：File Operations、Terminal & Processes、Web Search & Scraping、Memory、Skills、Session Search、Cron Jobs（按需）、Browser Automation（按需）。默认助理保留这些，再按任务增加 **Vision、Task Planning、Task Delegation**；Computer Use、图片/视频生成、Spotify、Home Assistant、X Search 等**用到再开**。每位固定搭档单独配一遍。

**网页服务**：建议先用**普通 Firecrawl**，同时负责"找网页"和"读正文"（点击 Web Search & Scraping 名称，在 Firecrawl 一行分别点"用于搜索""用于提取"）。三条接入路线：普通 Firecrawl / 自建 Firecrawl / Nous Subscription——**没有自建环境或 Nous 订阅就不要选后两项**。

**浏览器登录态**（重要安全点）：**设置 → Browser → Use My Real Browser Profile**——Hermes **复制**当前 Chrome/Edge/Brave/Chromium 的活动配置到**独立快照**，在后台使用已有登录状态，**不会直接占用正在浏览的配置目录**；每次新建浏览器会话时重新同步。作者明确警示：**"这个开关等于允许 Agent 以你的登录身份访问网站，只在确实需要的角色上开启"**；Windows 复制配置前还要彻底退出浏览器。

#### 2.3 性格、记忆与上下文

**三种"它知道的东西"**：SOUL.md 管**怎么说话、怎么做决定**；记忆保存**长期习惯**；文章、笔记和原始资料仍在**自己的资料库**。

- **SOUL.md 路径**：`hermes config path` 返回 `config.yaml` 位置，在其旁边新建 SOUL.md。默认位置 Mac/Linux `~/.hermes/`，Windows `%LOCALAPPDATA%\hermes\`；**每个固定角色都可以有自己的 SOUL.md**。
- 作者给的 SOUL.md 示例强调：先给判断和下一步再补理由；随手记只简短确认；不每步索取确认；**发现判断有问题直接指出依据，不为了顺着而附和**；需要选择时**优先给一个推荐并说清取舍**。

**记忆设置推荐值**：

| 设置 | 建议 | 为什么 |
| --- | --- | --- |
| 持久记忆 / 用户画像 | 都开 | 前者保存环境与长期约定，后者保存稳定偏好 |
| **记忆预算 / 画像预算** | **2200 / 1375 字符** | 这些内容**随每次请求进入上下文**；适合短而稳定的信息，**不适合塞文档全文** |
| 记忆提供方 | 仅内置 | 先存在本机 |
| 记忆写入审批 | 个人专用先关 | 保留自动积累；反复记错再开逐条确认 |

- **记忆文件位置**：同一配置目录下的 `memories/MEMORY.md` 和 `memories/USER.md`（可直接查看，也可直接说"展示你记住的关于我的偏好，把第二条改成……"）。
- **预算不够时的顺序**：**先删过期内容**，仍影响有用信息保存再小幅增加，**别一开始扩成几万字**。
- **审批开关**：`hermes config set memory.write_approval false`。CLI 可当场询问；**消息入口中待批内容需要用 `/memory pending` 查看，再用 `/memory approve 编号` 或 `/memory reject 编号` 处理**。
- ⚠️ 作者警示：**"开了审批却一直不处理，助理的记忆就会停在待确认状态。"**

**后台复盘**（任务结束后再让模型看一遍：哪些偏好、成功步骤或错误值得留到下次）：

```bash
hermes config set auxiliary.background_review.enabled true
hermes config set auxiliary.background_review.provider auto
hermes config unset auxiliary.background_review.model
```

- **代价**：自动复盘会增加模型用量。一次性任务为主或额度吃紧时设 `false`，需要时用 `/refine` 手动复盘。
- ⚠️ **同主模型的后台复盘会继承主任务的推理强度**——想降用量必须另选辅助模型。

**模型页三处容易误开**：**上下文窗口保持 0**（让 Hermes 自动读取）；**备用模型只在你已接好第二家模型服务时添加**；**Mixture of Agents**（多模型会诊）"效果可能更稳，但调用次数和费用也会增加，适合少量重要判断，不适合作为日常助理默认设置"。

**压缩设置**（"压缩只会把较早的聊天整理成摘要，不会压缩或删除资料库里的文件"）：

| 选项 | 推荐值 | 取舍 |
| --- | --- | --- |
| 上下文引擎 / 自动压缩 | Compressor / 开 | 避免越聊越大 |
| **压缩阈值** | **0.5** | 用到约一半上下文容量时开始压缩，给后续材料和工具结果留余量 |
| **保护最近消息** | **20** | 减少"刚指出的问题在压缩后丢了" |
| 压缩目标 | 先留 0.2 | 给后续对话腾空间 |

- **频繁处理长逐字稿且需要前后原话对照时才调到 0.7**，代价是每轮携带更多内容。
- ⚠️ **合同数字、引文和正式决定应落进文件，不能只依赖压缩摘要。**
- 压缩摘要本身也调用模型：`hermes config set auxiliary.compression.reasoning_effort low`

#### 2.4 权限三层（作者总结的框架）

| 层级 | 内容 | 推荐 |
| --- | --- | --- |
| **第一层 · 审批** | **设置 → 安全**：Smart / Manual / Off | **Smart，超时 300 秒，命令白名单留空** |
| **第二层 · 文件检查点** | `hermes config set checkpoints.enabled true` | **会反复改笔记/文档就开**；只查资料不改原文件的角色可关 |
| **第三层 · 执行环境** | 技能与工具 → 工具集 → Terminal & Processes | 处理自己电脑的文件选 **Local**；跑来路不明脚本时用 Docker 等隔离环境，只给必要文件夹 |

- **审批弹窗三种授权粒度**："仅此一次"（临时动作）／"本会话"／"始终允许"（形成长期规则）。⚠️ 作者警示：**"不要为了少点几次按钮，把宽泛命令加进白名单"**。
- **撤回方式**：`/rollback` 查看编号 → `/rollback diff 编号` 看差异 → `/rollback 编号 文件路径` 恢复。**只能恢复本地文件。**
- **无人值守时保留拒绝危险操作**：

```bash
hermes config set approvals.cron_mode deny
hermes config set approvals.unattended_mode deny
```

- "确认 MCP 重载""隐去密钥"保持开启；**"允许私有 URL"保持关闭**。

#### 2.5 唤起、通知与常驻

- **快速输入**：**设置 → 高级 → 快速输入**。Mac `⌘ + Shift + Space`，Windows `Ctrl + Shift + Space`（在浏览器、PDF 或笔记软件里唤起小输入框）。
- 输入框两个动作：`@` 添加文件/文件夹/网址；执行中 Mac `⌘ + Enter`、Windows `Ctrl + Enter` 把下一条**排到当前任务之后**；直接 Enter 则**立刻**交给正在执行的任务。
- **通知原则**：**只保留会改变下一步的事件**（需要批准、需要输入、本轮失败、额度提醒）。长任务放后台再保留"回复就绪"；完成提示太多就关掉"后台任务完成"和提示音。
- **工具日志**：**设置 → 外观 → 工具调用显示**选"产品"；排错或截图教程时再切"技术"。
- **时区**：`hermes config set timezone Asia/Shanghai`。⚠️ **"尤其是装在海外服务器上时，不要依赖服务器本地时区，否则'明天早上八点'可能按另一个时区执行。"**
- **保持电脑唤醒**：只能防止空闲休眠，**不保证 Mac 合盖后继续运行**。
- **Warm Bot Backends 留 2–3 个**：每多保留一个后台约多占 60 MB 内存。
- **网关切换**：**设置 → 网关 → 通过 SSH 连接**，桌面端自动建立加密连接，**不需要把服务端口暴露到公网**。⚠️ **每台网关都有自己的聊天、消息入口和定时任务；把桌面端从 Mac 切到服务器，并不会自动把原来的任务搬过去。**
- **消息显示设置（以 Telegram 为例，微信把 `telegram` 换成 `weixin`）**：

```bash
hermes config set display.platforms.telegram.tool_progress off
hermes config set display.platforms.telegram.show_reasoning false
hermes config set display.platforms.telegram.interim_assistant_messages false
hermes config set display.platforms.telegram.memory_notifications verbose
```

### 3. 核心能力实战

#### 3.1 固定搭档（BOTS）与接力

- 建研究员：**BOTS → ＋ 新建机器人**，Name `my-researcher`、Title `研究员`、Description `查官方来源，保留链接，把更新写成普通人能用的简报`。
- **高级 → General**：**Clone from profile 选 default**（复制默认助理的基础设置）；Provider 保持 **Inherit (launch profile)**、Model 留空；**Share keys & accounts with the main profile 保持勾选**；Create empty 先不勾；SOUL.md 先留空。
- **给能力做减法**：克隆 default 只为复用账户，**不要把它携带的全部 Skill 都留下**——研究员保留 grounded-citations、blocked-page-recovery、pdf、rss-feeds，再按第四章加 QMD、Blogwatcher；做图、写代码、音乐和邮箱 Skill 用不到就关。
- **并行子智能体填 3**："这是同时工作的上限，不是越大越聪明；普通订阅一次放出十个角色，更容易撞上并发限制"。
- 建 my-checker 做复核：研究员完成后输入 `@` 选择核查员检查同一份文件，再把问题交回研究员。**两个角色使用同一工作目录，才能围绕同一份成果接力。**
- **用 `/learn` 保存工作方法**：如"开头最多三项，先讲是否需要升级、具体用途、下一步操作；技术细节后置，保留版本日期和出处。**不要保存这次工具的版本号**"。
- **导出迁移**：

```bash
hermes profile export my-researcher -o my-researcher.tar.gz
hermes profile import ./my-researcher.tar.gz --name my-researcher
```

**记忆、性格、Skill 和配置随角色导入**；知识库目录需另行同步。

#### 3.2 定时任务

- 入口：主界面左侧 **定时任务**（Morning briefing、Weekly review、Topic news digest 等蓝图可直接改），或 **BOTS → 研究员 → Routines**。
- 关键设置：**打开 continuity（连续记住上次结果）**，让本轮参考自己的上次输出，**过滤已汇报过的内容**。
- ⚠️ **工作目录不能省略**：定时任务默认使用**网关启动时所在的目录**，不一定是你当前桌面会话的目录。**它也归属于创建它的网关；远端网关停机，桌面开着也不会替它执行。**
- 命令行等价写法：

```bash
hermes -p my-researcher cron create "every 1h" \
  "检查 https://github.com/NousResearch/hermes-agent/releases 的新正式发布，对照成果/更新简报.md 和上次输出。发现新版本时更新简报，只汇报新增内容；没有变化时简短说明，读取失败时报告原因。" \
  --name "工具更新检查" \
  --workdir "/你的完整路径/Hermes工作台" \
  --continuity --repeat 2 --deliver local
```

- 配套命令：`cron list` / `cron run 任务ID` / `cron pause 任务ID` / `cron resume 任务ID`。
- **多来源**：让各任务分别检查，再用一个汇总任务合并重复信息、标出更新时间，并**单列读取失败的来源**（`context_from` 链式任务）。

#### 3.3 微信随手记（"记一下 / 找一下 / 整理一下"）

作者说明此节受**金尘马**（[@jinchenma_ai](https://x.com/jinchenma_ai)）的微信随记文章启发。

**三个任务标记**（追加到 `.hermes.md`）：

- `"记一下："` → 内容存入**收件箱**，每条新建一份 Markdown；**正文保留原话**，日期和标题单独放，保存后回复文件路径。
- `"找一下："` → 搜索收件箱和资料库，给匹配的**原文片段与文件路径**；没有匹配就说明没找到。
- `"整理一下："` → 按本次要求加工指定材料，成品另存**成果目录**，附上用到的原笔记路径。

**接入微信**：

```bash
hermes -p my-researcher config set terminal.cwd "/你的完整路径/Hermes工作台"
hermes -p my-researcher gateway setup   # 向导里选 Weixin，手机微信扫码确认绑定
```

- ⚠️ **重要边界**：这里连接的是**腾讯 iLink Bot 私聊身份，不是把个人微信交给 Hermes 操作**。**普通微信群通常不能邀请这个 Bot，也不会向它投递群消息**——先把它当成自己的专用私聊入口。
- **配对审批**：首次私聊 Bot 可能返回 pairing code，需在电脑上执行 `hermes -p my-researcher pairing approve weixin 你的配对码`。
- **独立随记**：`hermes -p my-researcher config set platforms.weixin.extra.text_batch_delay_seconds 0`（默认等约 3 秒合并快速连发的文字；设 0 则逐条交给助理）。
- **开机自启**：向导最后会问是否立刻启动 Gateway、是否安装开机自动启动服务。**个人电脑长期作为助理主机，两个都选 Y**；临时试用则跳过服务安装，改用 `hermes -p my-researcher gateway run` 前台运行。**电脑仍需保持联网和唤醒。**

**作者自己的分层工作流**（与"记一下"配套）：

> 文章和链接先提取正文，留在 **Clippings 原文库**；随手记保留原话，落进 **Inbox**；选题直接进**灵感库**。只有确认值得长期吸收的内容，才进入**带出处的 Wiki**。真正准备创作时，再从知识库选回灵感库，确认立项。

> 🔗 该分层与本库 [[llm-wiki-三层架构]]（Raw → Wiki → Schema）及"带出处"原则**高度一致**，可作为个人知识流的另一实现样本。

### 4. 五个私人助理 Skill

| Skill | 解决的问题 | 安装/入口 |
| --- | --- | --- |
| **OpenCLI** | 让助理去**你已登录的网站**找真实反馈和原帖（连接已登录的 Chrome/Chromium） | `hermes skills install https://github.com/jackwener/OpenCLI/blob/main/skills/opencli-browser/SKILL.md` |
| **QMD** | **先翻旧资料再给新建议**——从文章、笔记、会议记录里找回相关原文 | 官方仓库 `optional-skills/research/qmd/SKILL.md`，技能中心搜 `qmd` |
| **Blogwatcher** | 保存**订阅与已读状态**，只告诉你新来的内容 | 官方仓库 `optional-skills/research/blogwatcher/SKILL.md` |
| **Email Inbox Triage** | 沿完整邮件线程找出**谁该行动、谁在等待**，先准备回复草稿 | **已内置**，技能页搜 `email-inbox-triage` |
| **Weekly Review Planning** | 对照一周记录，找出**停滞项目、答应过却没做的事、正在等的回复、下周排不下的计划** | **已内置**，技能页搜 `weekly-review-planning` |

**共同的配置纪律**（作者反复强调）：**第一次都先小范围试**（小资料夹 / 两个订阅源 / 三到五条邮件线程 / 三到五张票据），人工核对可靠后再扩大权限；**只读优先、不自动发送或删除**；**看不清的金额留给你确认，不要让它为了填满表格自动猜**。

**值得记录的用法细节**：

- **OpenCLI** 的验证方式很克制：先只让它"**读取当前网页标题验证连接，不发布任何内容**"。
- **QMD** 的提问范式："使用 qmd 找出我上次**没有采用**该工具的原因……**找不到旧依据就直说，不要替我补一个理由**"。
- **Weekly Review Planning** 的边界（作者提醒）：让它把"随口想到的点子"和"已经答应要做的事"分开，**只有后者进入待办；一句"以后想学摄影"不该自动变成下周必须完成的任务**。

### 5. 五位海外玩家的生活用法

| 玩家 | 场景 | 核心做法 |
| --- | --- | --- |
| **Gordon Guocheng Qian** | 学习 | 用 Hermes 回顾实际工作记录、通过周总结**接续进度**；每次结束记下"做会了什么、卡在哪里、下次先练什么" |
| **Brendan Tack** | 工作/旅行 | 把研究、项目简报、任务和成果放在一起，让后续决定落实到同一项目；旅行改期时更新行程与待办。**"只有我提供的预订凭据能证明已经订好，不要把候选方案当成订单"** |
| **Molly Lazarus** | 家庭日程 | 把家庭聊天中的邀请截图和学校邮件转给 Hermes，记下日期并**安排提前准备的事项**；给助理**独立收件地址**，只转发需要处理的邮件 |
| **Dave** | 菜单 | 每周选菜**继续参考之前的反馈**（味道、麻烦程度、还想不想吃）；再把菜单接到购物清单，只整理真正需要买的部分 |
| **himore** | 票据归档 | 照片/PDF/邮件/附件发给归档助理存入 [[obsidian|Obsidian]] 并返回位置；票据交给另一个 Bot 记录，月底生成报销表草稿 |

**社区补充来源**：Reddit `r/hermesagent` 的"反复检查积分机票、符合条件才通知"用法（用户 julp）。

### 6. 作者的核心主张

> **"工具会更新，模型也会换。只要资料、偏好和做事方法还在自己手里，每一次纠正就能让下一次少讲一句、少返工一步。"**

作者称之为 Hermes 的"**养成感**"——它越来越懂你，也始终是**你能看见、能修改、能带走**的长期搭档。

## 相关页面

- 实体：[[hermes]]（本页是其实操级来源）、[[grok-bot]]（对照：托管 vs 自托管）、[[obsidian]]（资料库与票据归档场景）
- 概念：[[skill文件]]、[[长期记忆]]、[[审批门]]、[[上下文压缩]]
- 主题：[[agent工程]]、[[自生长个人知识库]]、[[agent自动化获客]]
- 来源：[[agent自动化获客完整指南]]（hermes 的另一使用场景）

## 来源与待核实问题

- **来源**：https://x.com/noahduck283/status/2099445686731427941

### 待核实

- 作者 **@noahduck283（"诺鸭船长"）** 身份未核实。
- 文中提到的多数细节**均有官方文档链接、可信度较高**（作者逐处给了 `hermes-agent.nousresearch.com` 路径），但**本批未逐一打开核对**。具体包括：`/learn`、`/journey`、`/review`、`/refine`、`/rollback`、`/memory pending`、`profile export/import`、`cron create ... --continuity` 等命令与参数。
- **版本号 `v2026.9.7`** 为文中引用的官方文档 tag，未核实是否存在。
- **Intel Mac 不再受支持**：作者转述官方平台支持表，未直接核对。
- **微信接入的"腾讯 iLink Bot"**：作者已明确边界（iLink Bot 私聊身份，非个人微信代操作；普通微信群不投递），但**该 Bot 的企业/个人适用范围、是否对中国大陆以外地区开放未说明**。
- **原文正文存在明显的中英文重复段落**（多处一节内容出现两遍），疑为原文排版/机翻叠加，本页按语义去重，**未逐字保留重复部分**。
- 5 位海外玩家的用法**均为个人博客/帖子自述**，无对照数据；Reddit / LinkedIn 原文未逐条打开核对。
- **记忆预算 2200 / 1375 字符**为作者推荐值，非官方默认值（原文未说明是否与默认一致）。
- **本页与 [[hermes]] 实体页的分工**：本页收录"怎么用"的实操细节，实体页收录"是什么"的产品事实与网络核实结论；两者不重复。
