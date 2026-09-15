---
title: 变更日志
type: meta
aliases:
  - 日志
  - 更新记录
tags:
  - meta
  - 日志
created: 2026-08-17
updated: 2026-09-15
---

# 变更日志

本文件采用**只追加**方式维护，按时间倒序记录每次变更。**不修改、不删除历史记录。**

每条记录包含：日期、资料来源、新建页面、更新页面、待人工确认事项。

---

## 2026-08-17

- **日期**：2026-08-17
- **资料来源**：初始化搭建（无外部资料）
- **新建页面**：
  - `AGENTS.md`（维护规范）
  - `index.md`（全局索引）
  - `log.md`（本文件）
  - `wiki/sources/_template.md`
  - `wiki/concepts/_template.md`
  - `wiki/entities/_template.md`
  - `wiki/topics/_template.md`
- **更新页面**：无
- **待人工确认**：无

---

## 2026-08-17（增量维护 · 第 1 批）

- **日期**：2026-08-17
- **资料来源**：`raw/articles/用 Codex + Obsidian 搭建自生长的个人知识库实战.md`（作者苍何，2026-08-09 发布）
- **新建页面**：
  - `wiki/sources/codex-obsidian-自生长个人知识库.md`（来源摘要）
  - `wiki/concepts/llm-wiki.md`（概念）
  - `wiki/concepts/三层架构.md`（概念）
  - `wiki/entities/obsidian.md`、`workbuddy.md`、`codex.md`、`wesight.md`、`claude-obsidian.md`、`karpathy.md`、`canghe.md`（实体，共 7 页）
  - `wiki/topics/自生长个人知识库.md`（主题）
- **更新页面**：`index.md`（目录概览填充新页面链接）
- **待人工确认**：
  - WeSight「知识大脑」内测范围与正式发布时间
  - 文中模型版本（DeepSeek V4 Flash / Kimi K3 / Doubao-Seed-Evolving 等）能力与价格
  - Karpathy LLM Wiki 原始公开出处、苍何身份与蓝皮书地址

---

## 2026-08-17（网络检索核实 · 补充实体信息）

- **日期**：2026-08-17
- **资料来源**：网络检索（WebSearch），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/wesight.md`（补充 GitHub 地址、五重功能、安装配置、收费模式）
  - `wiki/entities/claude-obsidian.md`（补充 GitHub 地址、15 个 skill、命令、检索机制、安装方式）
  - `wiki/entities/canghe.md`（补充其为 WeSight 作者、别名「苍河」）
  - `wiki/sources/codex-obsidian-自生长个人知识库.md`（待核实项标记已核实）
- **待人工确认**：
  - 作者署名「苍何 / 苍河 / 苍老师」是否同一人及规范名
  - claude-obsidian 存在多个同名仓库（AgriciDaniel / LabinatorSolutions / alexdemenezes），主体与 fork 关系
  - WeSight「知识大脑」是否仍为会员内测

---

## 2026-08-17（结构优化 · 概念页更名）

- **日期**：2026-08-17
- **资料来源**：无（用户要求明确概念名，属结构性调整）
- **新建页面**：无
- **更新页面**：
  - 重命名 `wiki/concepts/三层架构.md` → `wiki/concepts/llm-wiki-三层架构.md`（title 改为「LLM Wiki 三层架构（Raw / Wiki / Schema）」）
  - 同步更新 9 处双链引用：`index.md`、`wiki/sources/codex-obsidian-自生长个人知识库.md`、`wiki/concepts/llm-wiki.md`、`wiki/topics/自生长个人知识库.md`、`wiki/entities/{obsidian,workbuddy,codex,wesight,claude-obsidian}.md`
- **待人工确认**：无
- **说明**：原「三层架构」名称过泛（易与软件三层架构混淆），改为「LLM Wiki 三层架构」；旧名「三层架构」保留为 alias，历史双链仍可解析。

---

## 2026-08-17（增量维护 · 第 2 批）

- **日期**：2026-08-17
- **资料来源**：`raw/articles/去AI味完整实战教程：从自查、改写到文风塑造的全部流程指南.md`（作者 @ai_Goge，2026-08-17 发布）
- **新建页面**：
  - `wiki/sources/去ai味完整实战教程.md`（来源摘要）
  - `wiki/concepts/去ai味.md`（概念）
  - `wiki/entities/stop-slop.md`、`humanizer-zh.md`、`shuorenhua.md`、`writing-style-skill.md`、`nuwa-skill.md`、`agent-style.md`（实体，共 6 页）
  - `wiki/topics/ai写作去味.md`（主题综述，含 Skill 全景分类表与完整工作流）
- **更新页面**：`index.md`（目录概览填充新页面链接）
- **待人工确认**：
  - 作者 @ai_Goge 身份
  - 文中多数 Skill 未给出完整 GitHub 链接，仓库地址与维护状态（stop-slop-zh、Humanizer-zh、qu-ai-wei、shuorenhua、ai-flavor-remover、De-AI-Prompt-Enhancer、humanize-mba-text-skill、AIWriteX 等）
  - 「AI 检测率」相关论断为作者经验观点，非定量结论

---

## 2026-08-17（网络检索核实 · 去 AI 味 Skill 仓库地址）

- **日期**：2026-08-17
- **资料来源**：网络检索（WebSearch），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/stop-slop.md`（补充 stop-slop-zh 多个同名仓库、英文版 stars/安装方式）
  - `wiki/entities/humanizer-zh.md`（补充英文原版 blader/humanizer + op7418/WoolenWang/idao-cube 三版）
  - `wiki/entities/shuorenhua.md`（补充 MrGeDiao/Jia-Hong-Peng/1-SKILL 三版）
  - `wiki/topics/ai写作去味.md`（新增「未单独建页项目的仓库地址」表，覆盖 qu-ai-wei、ai-flavor-remover、De-AI-Prompt-Enhancer、humanize-mba-text-skill、oh-story-claudecode、AIWriteX、taste-skill、两个检测项目）
  - `wiki/sources/去ai味完整实战教程.md`（待核实项标记已核实）
- **待人工确认**：
  - 多个同名多仓库（stop-slop-zh / Humanizer-zh / shuorenhua）的关系与优劣需甄别
  - 各 Skill 维护状态
  - 作者 @ai_Goge 身份

---

## 2026-08-17（确定同名 Skill 主推版本）

- **日期**：2026-08-17
- **资料来源**：GitHub API 客观数据（star / forks / pushed_at），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/stop-slop.md`、`humanizer-zh.md`、`shuorenhua.md`（明确主推版本 + star 依据）
  - `wiki/topics/ai写作去味.md`、`wiki/sources/去ai味完整实战教程.md`（待核实改为已确定）
- **确定结论（按社区口碑 star 数，均支持 Claude Code）**：
  - stop-slop-zh → `pencil20388-eng/stop-slop-zh`（41★，4 仓库最高，官方 issue 认可）
  - Humanizer-zh → `op7418/Humanizer-zh`（15481★，绝对领先）
  - shuorenhua → `MrGeDiao/shuorenhua`（1098★，仍在活跃维护）
- **用户约定**：Agent 环境为 Claude Code

---

## 2026-08-18（增量维护 · 第 3 批）

- **日期**：2026-08-18
- **资料来源**：`raw/articles/手调半小时的公众号排版，这篇25秒排完了.md`（作者达芬七 @davinci_seven，2026-08-17 发布）
- **新建页面**：
  - `wiki/sources/手调半小时的公众号排版.md`（来源摘要）
  - `wiki/entities/wechat-article-pipeline.md`、`gzh-design.md`、`davinci-seven.md`（实体，共 3 页）
  - `wiki/topics/公众号排版自动化.md`（主题综述，含工具生态表与三条工程底线）
- **更新页面**：
  - `wiki/entities/wesight.md`（gzh-design 加双链关联）
  - `index.md`（目录概览填充新页面链接）
- **待人工确认**：
  - 作者达芬七真实身份（仅自述"人在加拿大十年"）
  - xiaowan-wechat-layout、md2wechat 的仓库地址与协议
  - 六套主题视觉差异为作者主观描述

---

## 2026-08-18（网络检索核实 · 公众号排版底层项目）

- **日期**：2026-08-18
- **资料来源**：网络检索（WebSearch + GitHub 页面），非 Raw 层文件
- **新建页面**：
  - `wiki/entities/xiaowan-wechat-layout.md`（gzh-design 工作流增强层，AGPL-3.0）
  - `wiki/entities/md2wechat.md`（公众号发布 CLI，BUSL-1.1 商业授权）
- **更新页面**：
  - `wiki/topics/公众号排版自动化.md`（工具生态表补双链 + 协议）
  - `wiki/sources/手调半小时的公众号排版.md`（待核实项标记已核实）
  - `wiki/entities/wechat-article-pipeline.md`（两个底层项目加双链）
  - `index.md`（实体列表新增 2 页）
- **待人工确认**：
  - xiaowan-wechat-layout 作者署名「小晚 @bbkirstry」与 GitHub「@小晚不在」是否同一人
  - md2wechat 作者 X「@seekjourney」与 GitHub「geekjourneyx」对应关系

---

## 2026-08-18（网络检索核实 · 作者身份确认）

- **日期**：2026-08-18
- **资料来源**：网络检索（WebSearch + GitHub 个人主页），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/xiaowan-wechat-layout.md`（确认作者身份 + star 74）
  - `wiki/entities/md2wechat.md`（确认作者身份 + star 3.3k + 背景）
  - `wiki/topics/公众号排版自动化.md`、`wiki/sources/手调半小时的公众号排版.md`（待核实改为已确认）
- **确认结论**：
  - xiaowan-wechat-layout：小晚 = @小晚不在 = cyberxiaowan(GitHub) = @bbkirstry(X)，同一人
  - md2wechat：极客杰尼 = geekjourneyx(GitHub) = @seekjourney(X)，同一人

---

## 2026-08-18（网络检索核实 · 达芬七身份）

- **日期**：2026-08-18
- **资料来源**：网络检索（WebSearch），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/davinci-seven.md`（补充背景：定居魁北克、十年移民、前 996 程序员、Stanley-Team 成员；xiaowan/md2wechat 加双链）
  - `wiki/sources/手调半小时的公众号排版.md`（达芬七身份待核实改为已核实）
- **结论**：达芬七 = @davinci_seven，定居加拿大魁北克华人，2014–2026 十年移民，前国内 996 程序员，内容方向为 AI/润学。

---

## 2026-09-12（增量维护 · 第 4 批）

- **日期**：2026-09-12
- **资料来源**（`raw/articles/`，共 3 篇未维护文章）：
  1. `10 个 Skill 搭建日更爆文的公众号写作系统.md`（@kongge_space，2026-08-27 发布）
  2. `从 intent.md 到闭环：AI 原生软件开发的六个阶段、一条产物链、几道审批门 原创.md`（@shao__meng 解读 Anthropic《The AI-Native SDLC playbook》，2026-09-02 发布）
  3. `万字长文  Agent 工程解析（一）：上下文管理.md`（@coder_left，2026-09-12 发布）
- **新建页面**：
  - 来源摘要（3）：`wiki/sources/10个skill搭建公众号写作系统.md`、`从intent到闭环-ai原生sdlc.md`、`agent工程解析-上下文管理.md`
  - 主题（3）：`wiki/topics/公众号内容创作系统.md`、`ai原生软件开发.md`、`agent工程.md`
  - 概念（13）：`ai原生sdlc.md`、`意图文件.md`、`产物链.md`、`审批门.md`、`建议性控制与确定性控制.md`、`eval-套件.md`、`上下文管理.md`、`上下文窗口.md`、`长期记忆.md`、`kv-cache.md`、`注意力机制.md`、`agent-loop.md`、`上下文压缩.md`
  - 实体（7）：`creator-buddy.md`、`anthropic.md`、`claude-code.md`、`openai.md`、`louis-claxton.md`、`shao-meng.md`、`coder-left.md`
- **更新页面**：
  - `index.md`（目录概览新增 26 条链接，updated 改为 2026-09-12）
  - `wiki/topics/公众号排版自动化.md`（补 [[creator-buddy]] / `space-wechat-layout` 同类能力说明，加主题双链）
  - `wiki/topics/ai写作去味.md`（补 [[creator-buddy]] 及 `gzh-short-post` 去 AI 腔关联）
- **维护决策（经用户确认）**：
  - 文章 1 的 10 个 Skill 采用**合并式**：建 `creator-buddy` 一个实体页收录，主题页用表格列出，不逐页拆分（信息量小，与去 AI 味一文"信息少不建页"做法一致）。
  - 已提交进 `raw/` 但 wiki 从未维护的《从 intent.md 到闭环》**一并处理**。
- **待人工确认**：
  - `creator-buddy`（SpaceZephyr/creator-buddy）的 LICENSE、Skill 完整性与维护状态；作者 @kongge_space 身份。
  - 《Agent 工程解析》中大量 Claude Code 内部实现细节（Snip compact / Micro compact / Context collapse / 各 Token 阈值）为作者对公开实现的推测，需与官方文档核对。
  - 《从 intent.md 到闭环》为中文解读，原文（英文手册）未入库，产物链/托管设置等表格需与原文校对。
  - 新增人物页（`shao-meng`、`coder-left`、`louis-claxton`）背景未做网络检索核实。
  - 公众号商单"报价 = 平均阅读量 × 2"与收入数字为作者个人经验，非普适结论。

---

## 2026-09-12（网络检索核实 · AI 原生 SDLC 与上下文机制）

- **日期**：2026-09-12
- **资料来源**：网络检索（WebSearch + WebFetch 原文），非 Raw 层文件
- **更新页面**：
  - `wiki/sources/10个skill搭建公众号写作系统.md`、`wiki/entities/creator-buddy.md`（核实作者身份、仓库协议/热度/安装/使用边界、Skill 数量修正、第三方衍生 GZH Buddy）
  - `wiki/sources/从intent到闭环-ai原生sdlc.md`、`wiki/concepts/ai原生sdlc.md`（原文已取到并核对；play 计数口径；术语别名）
  - `wiki/entities/anthropic.md`、`wiki/entities/claude-code.md`（Claude Tag / Claude Security / Cowork 状态；1M 窗口型号）
  - `wiki/concepts/上下文压缩.md`（**新增第五节「不同来源的说法差异」**，并列保留多种口径）
  - `wiki/concepts/上下文窗口.md`、`wiki/entities/openai.md`（1M 窗口型号核实）
  - `wiki/concepts/eval-套件.md`（补官方 CI 示例 `agent-evals.yml`）
  - `wiki/entities/shao-meng.md`、`wiki/entities/coder-left.md`（作者身份核实结果）
- **确认结论**：
  - **creator-buddy**：作者 = 空格.space（@kongge_space = GitHub「空格的键盘」）；仓库 `SpaceZephyr/creator-buddy` 含公众号 / 小红书 / 视频三条产品线；README 声明 MIT 但**根目录无 LICENSE 文件**；`gzh-Skills` 实测 12 个（帖子列举 10 个）。
  - **Anthropic 手册**：原文确为 Louis Claxton 2026-08-21 发布，致谢 Jim Blackhurst / Will Steuk / Jamal Arif；6 个阶段、约 16 个 play 条目；术语亦称 **agentic SDLC / AI SDLC**。
  - **1M 上下文窗口** = Claude Opus 4.6 / Sonnet 4.6（约 2026-03 GA）。
- **保留分歧（分歧并存）**：Claude Code 上下文压缩机制的**层数**（4 / 5 / 6）、**命名**（Full compact / AutoCompact / Reactive compact / Traditional compact）与**阈值**（93%、80% / 78%）在不同来源间不一致，已在 `上下文压缩.md` 第五节并列保留，**未取单一结论**。
- **待人工确认**：
  - creator-buddy 仓库无 LICENSE 文件；"三年三万粉、月入一两万"仍为作者自述。
  - @coder_left（程序员 Left）身份检索未获可靠资料；@shao__meng 具体身份未证实（其解读帖被 BitTide 等聚合站收录）。
  - 部分中文二手解读转述的背景数字（如"Anthropic 内部约 80% 合入代码由 Claude 完成"）未见原文出处。

---

## 2026-09-14（增量维护 · 第 5 批）

- **日期**：2026-09-14
- **资料来源**（`raw/articles/`，共 2 篇未维护文章）：
  1. `写作指南：让 AI 写作无限接近你的真实文风.md`（@SenMufs，2026-09-13 发布）
  2. `越改越烂！为什么 AI 自动修改 UI 总是翻车？「附终极解法」.md`（@Lonely__MH，2026-09-13 发布）
- **新建页面**：
  - 来源摘要（2）：`wiki/sources/写作指南-ai真实文风.md`、`ai改ui翻车.md`
  - 主题（1）：`wiki/topics/ai生成ui.md`
  - 概念（2）：`wiki/concepts/个人写作风格库.md`、`视觉自愈循环.md`
  - 实体（3）：`wiki/entities/chatgpt.md`、`ling-3-flash-vl.md`、`taste-skill.md`
- **更新页面**：
  - `index.md`（目录概览新增 8 条，updated 改为 2026-09-14）
  - `wiki/topics/ai写作去味.md`（**新增「两条技术路线（分歧并存）」**；taste-skill 建页后改链接；相关页面与来源补充）
  - `wiki/concepts/去ai味.md`（第 3 层补两条实现路径；相关页面补充）
  - `wiki/entities/writing-style-skill.md`（新增「与 ChatGPT Writing Style 的关系：同源异流」）
  - `wiki/entities/openai.md`（补 [[chatgpt]] 产品条目）
  - `wiki/concepts/ai原生sdlc.md`（Test 阶段交叉引用 [[视觉自愈循环]]）
- **保留分歧（分歧并存）**：文章 1 明确否定"靠提示词与去 AI 味 Skill"的路线，与本库既有的 Skill 组合路线构成对立。已在 `ai写作去味.md` 新增「两条技术路线」表并列保留（**Skill 组合派 vs 真实样本派**），**不取单一结论**，并指出二者共享"增加作者信息"的终点。
- **待人工确认**：
  - 两篇作者（@SenMufs、@Lonely__MH）身份未核实。
  - ChatGPT Writing Style 的可用范围与地区限制；效果为作者自述、无对照实验。
  - 原文目录名拼写不一致（`Eian Writing Corpus` / `EWriting Corpus`），**疑为笔误**，页面已保留原样并标注。
  - Ling-3.0-flash-VL 的参数与"限免 2 周"为转引；"7 秒"为单次非受控记录。
  - UI 自愈实验仅两张卡片、两次录屏，作者自述"说明不了统计规律"。

---

## 2026-09-15（增量维护 · 第 6 批）

- **日期**：2026-09-15
- **资料来源**（`raw/articles/`，共 2 篇未维护文章）：
  1. `为什么你手握 Codex、Claude，依然赚不到钱？.md`（@Huouo908070，2026-09-14 发布，观点文）
  2. `如何使用 Agent 自动化获客（完整指南）.md`（原文 Chris Everest @everestchris6，中译 @yibie，2026-09-14 发布）
- **新建页面**：
  - 来源摘要（2）：`wiki/sources/为什么手握codex-claude依然赚不到钱.md`、`agent自动化获客完整指南.md`
  - 主题（2）：`wiki/topics/ai创业与需求发现.md`、`agent自动化获客.md`
  - 概念（2）：`wiki/concepts/需求三等级.md`（好奇 / 麻烦 / 正在花钱解决）、`skill文件.md`（Agent 可移植工作流文档）
  - 实体（5）：`wiki/entities/chris-everest.md`、`grok-bot.md`、`hermes.md`、`apify.md`、`whop.md`
- **更新页面**：
  - `index.md`（目录概览新增 11 条，updated 改为 2026-09-15）
  - `wiki/topics/agent工程.md`（主题边界新增与 [[agent自动化获客]] / [[skill文件]] 的层次说明）
- **维护决策**：
  - **不建页（信息量小）**：@Huouo908070、@yibie（仅在来源页标注待核实，与第 5 批 @SenMufs / @Lonely__MH 处理一致）；replicate、fal、gpt image 2.5、seedance 2.5、Railway、@BotFather（在主题页工具栈表格收录）。与前几批"信息少不建页"的决策保持一致。
  - **跨文章关联**：文章 2 的核心方法"找到已经在付钱的人"被判定为文章 1 [[需求三等级]]第三级的**操作化落地**，两个新主题页已互相建立双链（`ai创业与需求发现` ↔ `agent自动化获客`）。
  - **合规提示保留**：文章 2 自带"冷启动触达与数据抓取受地区法规/平台规则限制"声明，已在来源页与主题页**原样保留**并前置警示。
  - **命名消歧**：`hermes` 实体页明确"仅指来源描述的常驻计划任务 Agent 服务"，与 Nous Research Hermes 模型等同名项目的关联标注为未知；`grok-bot` 是否指 xAI Grok 的 agent 形态标注待核实。
- **保留分歧（分歧并存）**：本批未发现与既有页面冲突的事实性分歧。文章 1"技术不再稀缺、稀缺的是需求判断"与本库既有主题（agent工程、自生长个人知识库等聚焦"怎么用好 AI"）构成**视角互补而非对立**，已在主题页以关系表说明，未取舍。
- **待人工确认**：
  - @Huouo908070、@yibie 身份未核实。
  - `grok-bot` / `hermes` 的产品指向与仓库地址（hermes 名称过泛）。
  - "gpt image 2.5 / seedance 2.5 为最佳图像/视频模型"（作者 2026-09 时点个人判断）；"明信片效果远好于邮件/短信"（作者个人测试无对照数据）；"whop ads 处于 Meta 最高层级、被拒更少"（作者说法，未对官方文档核对）。
  - [[skill文件]] 与 Claude Code Agent Skills 机制的兼容关系为**推断**（原文未说明）。
  - 获客方法的合规边界（平台抓取规则、各地区短信/邮件营销法规）落地前需逐项确认。
  - 两篇均为单一来源观点/指南，无第三方复现记录。

---

## 2026-09-15（网络检索核实 · grok-bot 与 hermes 实体指向）

- **日期**：2026-09-15
- **资料来源**：网络检索（WebSearch + GitHub API），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/grok-bot.md`（**身份核实 + 全面扩写**：xAI Grok Bot，2026-08-11 beta，持久云 VM（浏览器/文件系统/终端），Cursor/SuperGrok 账号认证，$200–300/月，官方文档 docs.x.ai/grok-bot，skills/routines/审批门机制，安全注意事项）
  - `wiki/entities/hermes.md`（**身份核实 + 全面扩写**：Nous Research 的 Hermes Agent，开源 `NousResearch/hermes-agent`，**MIT，245,618★ / 51,198 forks**（GitHub API 2026-09-15 快照），创建 2025-07-22、当日仍在推送；Telegram 等多渠道 gateway、cron 计划任务、`~/.hermes/skills/.../SKILL.md`、Railway 一键部署；命名消歧：Hermes Agent ≠ Hermes 模型系列，同司不同产品）
  - `wiki/concepts/skill文件.md`（"与 Claude Code Skill 机制的关系（推断）"升级为"与各生态 Skill 机制的关系（已核实）"：Claude Code / Grok Bot / Hermes 三生态均有 skill 机制支撑可移植性主张；跨生态直接复用仍待实测）
  - `wiki/sources/agent自动化获客完整指南.md`、`wiki/topics/agent自动化获客.md`（待核实项标记已核实）
- **确认结论**：
  - **grok bot = xAI 的 Grok Bot**：与来源文章描述（自带电脑/终端/浏览器/文件系统、像聊天一样交互、给 skill 文件即可跑）完全吻合；产品含原生 skills（演示保存 / marketplace / Private Plugins 安装）与 routines 定时能力。
  - **hermes = Nous Research 的 Hermes Agent**：与来源文章描述（为计划任务而建、部署 Railway、@BotFather token、Telegram 交互）完全吻合；按本库惯例补充 stars/recency 客观指标（245k★、活跃维护）。
- **保留分歧（分歧并存）**：
  - Grok Bot 开发方表述：官方文档署名 xAI；部分新闻称 "SpaceXAI"（xAI–SpaceX 合并实体）并提及 2026-08-14 完成 Cursor 收购——两种口径并列，以官方为准。
  - Grok Bot 平台覆盖：cual.ai 称无 Linux/Android/iPad 版；windowsmode 称有 Linux 原生版——并列保留。
- **待人工确认**：
  - 来源文章"投喂任意 skill .md 文件即运行"的具体导入路径未在 Grok Bot 官方文档逐字核实。
  - Chris Everest 文中所述"用 prompt 让 Claude 部署 hermes"路径与现行 Railway 图形化模板并存的细节未复现。
  - 定价/套餐为 2026-08/09 新闻口径，可能变动；star 数为当日快照。

---

## 2026-09-15（网络检索核实 · whop 与 Apify）

- **日期**：2026-09-15
- **资料来源**：网络检索（WebSearch + 官方文档 + GitHub API），非 Raw 层文件
- **新建页面**：无
- **更新页面**：
  - `wiki/entities/whop.md`（**核实 + 全面扩写**：Whop Ads 官方文档逐条核对，新增基本信息、来源说法 vs 官方文档对照表、已核实机制；官方文档 docs.whop.com）
  - `wiki/entities/apify.md`（**核实 + 全面扩写**：官方 MCP `apify/apify-mcp-server`（MIT，7,185★）、5,000+ Actors、套餐与计费、各平台 scraper 对照表、合规边界）
  - `wiki/sources/agent自动化获客完整指南.md`、`wiki/topics/agent自动化获客.md`（待核实项标记已核实；主题页工具栈表格增加"核实状态"列）
- **确认结论（重要：作者说法获官方文档背书）**：
  - **Whop Ads 的"Meta 最高层级账号"说法为真**：官方文档明确写 **Platinum-tier HIVA（Meta's highest tier）— priority bidding and lower cost per thousand impressions at scale**，被拒更少（"Fewer thanks to higher account standing"）、有直接 Meta 代表。来源文章措辞与官方口径几乎逐字一致。
  - **Whop Pixel = 第一方归因**：官方称 Whop 拥有底层支付栈，pixel 用真实支付数据而非浏览器信号归因，并通过 Conversions API 回传 Meta。
  - **Whop 出资三方式**：信用卡（2.9% 手续费）／Whop Card（免手续费 + 广告支出 5% 返现）／Pending Whop balance（未结算收入当天可用）。使用 Whop Ads 无平台费、无月费、无最低消费。
  - **Whop Ads 上线 2026-05-12**；当时仅 Meta（Facebook + Instagram），TikTok / Google / Snapchat / X / Reddit 标注 coming soon。
  - **Whop 违规清单与来源一致**：Fake or unverifiable income claims / Fake testimonials / Scam-style or deceptive offers，投前跑内置合规检查。
  - **Apify 官方 MCP 存在**：`apify/apify-mcp-server`，**MIT，7,185★**，2026-09-14 仍在推送。
  - **Apify 计费**：按 CU（$0.20/CU）+ Actor 用量；Free 档 $5 额度/月（每月重置、无需信用卡）／Starter $29／Scale $199／Business $999。
  - **Apify 合规口径**：只抓公开可见页面、不做登录绕过；**LinkedIn 与 Facebook 登录态数据需先取得书面许可**；个人数据一律触发 GDPR/CCPA。这与来源文章自带的合规声明**相互印证**。
- **保留分歧（分歧并存）**：
  - **Whop 每日消费上限**：官方文档称 agency 账号"无消费上限"，而 whatpayment 解读称"账号从 Day 1 上限逐步爬坡（1–2 周）"——两者表述不一致，可能为文档与实操阶段差异，已并列保留。
- **待人工确认**：
  - Whop 素材尺寸"Meta 三种尺寸比例"未在官方文档核实。
  - Meta 转向 invoice-only 计费的影响（whatpayment 提及，官方未在本批页面说明）。
  - **平台适用范围**：Whop 是否对中国大陆卖家开放、支持哪些支付方式（含出款）——**对国内落地是硬约束**，未获信息。
  - Apify 各平台 Actor 的价格/评分为第三方整理的 2026-05 快照，非官方推荐；来源文章未指明所用具体 Actor。

---

## 2026-09-15（网络检索核实 · lieflat-less-ai-tone 仓库）

- **日期**：2026-09-15
- **资料来源**：网络检索（WebFetch 读取仓库 README / SKILL.md 原文 + GitHub API），非 Raw 层文件
- **新建页面**：
  - `wiki/entities/writing-dna-skill.md`（实体，写作蒸馏器——`lieflat-less-ai-tone` 的配套项目）
- **更新页面**：
  - `wiki/entities/lieflat-less-ai-tone.md`（**核实 + 全面重写**：仓库指标、语料规模、11 项通过表、15 项未通过表、模型间差异表、SKILL.md 11 条规则全表、六次测量失误、六项自陈局限、复算方式、同作者仓库列表）
  - `wiki/entities/moxt.md`（**核实 + 重写**：Moxt = moxt.ai，"组建 AI 团队承担长程复杂工作"的平台；四个组成部分；与 [[可内省性]] 的 Markdown/HTML/CSV 主张相印证）
  - `wiki/sources/去ai味语料实证研究.md`（待核实项逐条结算；**修正 "GPT 5.6 Sol 系笔误"的判断**；补齐原图片中的完整数据表）
  - `wiki/concepts/去ai味.md`（"特征的实证检验"一节标注已核实；补充关键细节与**测量失误警示**；相关页面扩充）
  - `wiki/topics/ai写作去味.md`（**新增「一个已落地的多路线协同样本」**；Skill 分类表增列 writing-dna-skill；待核实清单逐条结算）
  - `index.md`（实体列表新增 1 条）
- **确认结论**：
  - **仓库存在且公开**：`larashero3-dotcom/lieflat-less-ai-tone`，**MIT，780★ / 56 forks**，创建 **2026-08-20**，最后推送 **2026-08-24**，主要语言 **Python**，未归档。
  - **全部统计数字与 README 逐一对照一致**：629 篇 / **2,826,972 汉字** / 95,551 句 / 45,721 段（生成 300 篇 117.9 万字；人类 329 篇 164.8 万字）；生成侧覆盖 **38 个话题**；11 项通过、15 项未通过。
  - **SKILL.md 可完整读取**：**11 条改写规则** + 「硬性边界（最高优先级）」+ 「不作为改写理由」**硬约束** + 最终验收清单。
  - **曾担心的"规则与结论不自洽"经查不成立** —— 被证否的特征（设问、比喻总数、句长/段长均匀度、句内同构排比、单字虚词、被动句、名词化与长句本身、正文"首先…其次"）**不仅未进入改写清单，还被单列为"不作为改写理由"的硬约束**。
  - **六次测量失误已公开**（README 第 5 节），其中**四项若未修正将直接进入规则集，两项方向相反**——"据以改写将使文本更偏离人类写作特征"。由此确立规程：**改规则前先抽样检视 20 条命中**。
  - **Moxt 已确认**：Moxt（moxt.ai），"组建 AI 团队来承担长程复杂工作的平台"，含工作流 / Agent 看板 / 小程序 / AI 原生工作空间四部分。**Skill 在 Moxt 上制作，并推荐在 MoxtHub 运行。**
  - **配套项目 `writing-dna-skill`（写作蒸馏器）已核实**：MIT，**1,832★ / 180 forks**，创建 2026-06-27（**早于** lieflat-less-ai-tone），**已内置本规则集**。
  - **作者账号**：`larashero3-dotcom`（GitHub 显示名 **"lieflat"**，204 followers，2026-02-07 注册，**10 个公开仓库**）。
- **重要修正（推翻本库此前判断）**：
  - ~~"GPT 5.6 Sol" 疑为笔误~~ → **非笔误**。`gpt-5.6-sol` 是仓库中的正式模型标识（与 `claude-opus-4-6`、`deepseek-v4-pro`、`gemini-3.1-pro`、`kimi-k3` 并列）。**但其是否为官方公开发布的真实版本名仍待核实**——这与第 7/8 批对 "seedance 2.5"（已判为笔误）的处理**方向相反**，两者不应混为一谈。
- **新增知识贡献（本批最有价值）**：[[ai写作去味]] 主题首次出现「**多路线协同的已落地样本**」——
  - `writing-dna-skill`（**风格逼近**，第一道工序）**内置** `lieflat-less-ai-tone`（**清除生成痕迹**，第二道工序），"装该仓库即随行"。
  - 并给出**冲突裁决规则**："同目录存在蒸馏产物时优先读取 `语言DNA.md`；**两者冲突时以蒸馏产物为准**，因其记录的是目标作者的实际写法，不属生成痕迹"。
  - 举例说明其效果："**某作者本来就爱用破折号，就不该按第 4 条删掉**"（破折号 *R*=3.0 本属显著特征，但对该作者失效）。
  - → **这为本库"三条路线应当并用"的建议提供了可引用的实现依据**：实证派提供判据，真实样本派提供边界，二者不冲突。
  - → 同时为 [[可内省性]] 提供了**跨来源印证**：Moxt 明确选择 **Markdown / HTML / CSV** 作为"AI 原生"文件格式，与 Ronacher 的"Markdown / JSON / Unix 管道在赢，因为人能看懂"**指向同一结论**。
- **同作者的方法论产品线（已核实 API 元数据）**：`lieflat-charts`（5,384★）、**`writing-dna-skill`（1,832★）**、`lieflat-gongwen`（961★，**102 万字语料的公文写作 Skill**，"把公文写作风格变成可测量、可验收的量化数据"）、`lieflat-less-ai-tone`（780★）、`lieflat-html-design`（87★）、`soul.skill`（49★）、`lieflat-ai-knowledge-base`（13★）、`lieflat-cards`（10★）、`yingxian-pagoda`（2★）。
  - 📌 **观察**：该作者有一套**成体系的"语料量化 → 可验收规则"产品线**（less-ai-tone 与 gongwen 同思路）。**本批暂不建"方法论体系"实体页，待补充来源后再定。**
- **保留分歧（分歧并存）**：
  - **同作者的 star 分布差异显著**：`lieflat-charts` 5,384★ 与 `lieflat-less-ai-tone` 780★ 相差近 7 倍，但**后者是前者的研究方法论最完整的呈现**——**热度不等于方法论价值**，本库按"方法论可追溯性"收录，不以 star 排序。
  - **两条路线之争新增一个具体解**：`writing-dna-skill` 的"样本优先于规则"不是对规则派的否定，而是**为规则划定边界**——本库此前只并列保留三种立场，**现在可以记录一个已被产品化的折中方案**，但仍**不取单一结论**。
- **待人工确认**：
  - **@Zhiyu333 与 GitHub `larashero3-dotcom`（"lieflat"）的对应关系**——推测同一人（文中即给出该仓库），**未找到直接证据**；账号名与"躺平"的关联亦未说明。
  - **五个模型标识是否为官方正式版本名**（`gpt-5.6-sol` 等）——未对官方模型列表核实。
  - **语料不可核验**（作者自陈"第三方无法直接复核"）；**`scripts/` 三个脚本未逐行审阅**。
  - **统计方法未经同行评议**：阈值为作者自定；**未检索到第三方复现**。
  - **`moxt.ai` 官网本批未直接打开**——开发方、计价、地区可用性未核实；**Moxt 与作者的关系深度未证实**（README 由同一账号发布，存在作者为 Moxt 相关方的可能）。
  - **`writing-dna-skill` 的 README / SKILL.md 未读取**——蒸馏方法与 `语言DNA.md` 格式未核实。
  - **同作者其他 7 个仓库仅取 API 元数据**，未读取 README；"同一套语料量化方法论"的判断为**基于仓库描述的推断**。
  - 仓库较新（subscribers 仅 1、无 topics），长期维护待观察。

---

## 2026-09-15（增量维护 · 第 8 批）

- **日期**：2026-09-15
- **资料来源**（`raw/articles/`，共 3 篇未维护文章）：
  1. `做了一个可能有最多数据支撑的去 AI 味 skill.md`（@Zhiyu333，2026-09-15 发布，语料实证研究）
  2. `养成系私人助理 Hermes｜从入门到榨干.md`（@noahduck283，2026-09-14 发布，实操手册）
  3. `爆款复刻｜月涨粉 5w 还能出海赚美金？拆透「古风武侠英语剧」的长青打法与搞钱闭环.md`（@CrazyKaomei，2026-09-15 发布）
- **新建页面**：
  - 来源摘要（3）：`wiki/sources/去ai味语料实证研究.md`、`hermes私人助理养成指南.md`、`爆款复刻-古风武侠英语剧.md`
  - 主题（1）：`wiki/topics/ai自媒体爆款复刻.md`
  - 概念（2）：`wiki/concepts/ai味特征实证.md`、`反差选题法.md`
  - 实体（4）：`wiki/entities/lieflat-less-ai-tone.md`、`moxt.md`、`kaomei.md`、`doubao.md`
- **更新页面**：
  - `index.md`（目录概览新增 10 条，updated 改为 2026-09-15）
  - `wiki/entities/hermes.md`（**依据新的实操来源大幅扩写**：官方文档站、安装命令、命令与入口速查表、关键配置推荐值表、三层权限框架、BOTS 角色分工、5 个私人助理 Skill、与来源页的分工说明；sources 增列 `hermes私人助理养成指南`）
  - `wiki/topics/ai写作去味.md`（**「两条技术路线」升级为「三条技术路线」**，新增实证派；新增「实证派对前两条路线的具体影响」纠正表、「实证研究的方法框架」表；Skill 全景分类表增列 `lieflat-less-ai-tone`；相关页面与待核实清单扩充）
  - `wiki/concepts/去ai味.md`（新增「特征的实证检验」一节，列出被证否的流行认知与显著项排序；sources 增列；相关页面与「保留分歧」三条路线说明）
  - `wiki/topics/agent自动化获客.md`（Agent 选择行补充 Hermes 的另一面）
- **维护决策**：
  - **`moxt` 破例建页**：本库既有惯例是"信息少不建页"，但 Moxt 在来源文章中是**方法论执行的关键载体**（作者定标准 → Moxt 做枚举与统计），非可有可无的提及；建页便于后续增量合并。页面明确标注"推断部分不得作为事实引用"，并给出**将来可并入来源页**的退路。
  - **`hermes` 实体页与来源页分工**：实体页收录"是什么"（产品事实 + 网络核实结论），来源页收录"怎么用"（安装/设置/BOTS/微信/5 个 Skill/5 位海外玩家用法），**明确写进两页，避免重复**。
  - **`doubao` 建页而非仅在来源页标注**：因豆包同时出现在 [[10个skill搭建公众号写作系统]]（AI 写作/配图）与本批来源（短视频全流程），具备**跨来源**特征；并与既有的 [[fal]] / [[replicate]] 构成"同一批模型的不同接入层"的对照关系。
  - **`kaomei` 建页**：作者自曝 3 个开源 Skill 并主理系列专栏，具备可累积的实体特征。
  - **不建页（信息量小）**：@Zhiyu333、@noahduck283（诺鸭船长）、金尘马 @jinchenma_ai、Chris Everest 文中已建页、@SenMufs 等；5 位海外玩家（Gordon / Brendan / Molly / Dave / himore）仅在来源页收录。
  - **跨文章关联**：本批第 3 篇的"高付费意愿人群"被判定为 [[需求三等级]] 第三级在**内容赛道**的应用；其作者价值观（"大模型给了所有人 70 分入场券"）与 [[ai创业与需求发现]]、[[可内省性]] 构成**三来源呼应**，已在主题页记录。
- **保留分歧（分歧并存，本批核心贡献）**：
  1. **本库去 AI 味主题首次记录「三条技术路线」**：Skill 组合派 vs 真实样本派 vs **实证派**。实证派的价值不只是补充——它**用数据证否了若干流行规则**（"减少设问"、"减少比喻"、"句子长度太均匀"），并据此指出前两条路线的依据（"个案观察与凭语感的总结，没有被系统检验过"）**可能不可靠**。已在 `ai写作去味.md` 与 `去ai味.md` 并列保留，**未取舍**。
  2. **描述精度差异**：[[反差选题法]]（"反差越大越好"，无量化方法）与 [[ai味特征实证]]（有倍数阈值，无传播学判据）**恰好互为镜像**——一个给判据不给方法，一个给方法不给判据。已在 `反差选题法.md` 明确标出并并列保留。
  3. **Hermes 自我定位的两种叙事**：Chris Everest 视其为"为计划任务而建"的获客执行器；@noahduck283 视其为"能带走"的私人助理。**同一产品、不同用途**，已在实体页以"三个使用场景"表并列。
- **重要核实发现（无，但有三处明确存疑）**：
  - **"GPT 5.6 Sol"** 这一模型命名与既有版本惯例（[[openai|GPT-5.x]]）不符，已在来源页与概念页标注**待核实**。
  - **"gpt image 2.5 / seedance 2.5" 的同类问题**（第 7 批已记录）在本批第 3 篇中得到部分呼应：本文出现 **"Seedance 2.0 Fast"**（与 [[fal]] 页记录一致），**不排除 Chris Everest 文中的 "2.5" 为笔误**——两批来源交叉对照，**倾向支持"2.5 系笔误"的判断**，但仍未定论。
  - **`larashero3-dotcom/lieflat-less-ai-tone` 仓库未做检索核实**（本批未执行网络检索）。
- **待人工确认**：
  - 三位新作者 **@Zhiyu333、@noahduck283（诺鸭船长）、@CrazyKaomei（烤妹儿）** 身份均未核实。
  - **`lieflat-less-ai-tone`**：仓库是否存在/可访问/License/star/维护状态；**SKILL.md 实际规则清单**（无法判断是否误留了被作者自己证否的规则）；**Moxt 是什么**。
  - **全部定量结论无第三方复现**：283 万字语料的统计结果；短视频赛道的所有数据（20 万赞、27.4 万粉、完播率 40%、佣金 50%~70%、TikTok 24w 粉）。
  - **Hermes 实操细节未逐一对官方文档核对**：`/learn`、`/journey`、`/review`、`/refine`、`/rollback`、`/memory pending`、`profile export/import`、`cron --continuity`、`gateway setup`、`pairing approve` 等命令；记忆预算 2200/1375、压缩阈值 0.5、审批超时 300 秒等推荐值；文档 tag `v2026.9.7`；**Intel Mac 不再支持**的转述。
  - **微信（腾讯 iLink Bot）适用范围**（是否对中国大陆以外开放）未核实；**xAI Grok OAuth 接 SuperGrok / Premium+** 未核实。
  - **反向出海的准入与收款**（TikTok / YouTube Shorts 创作者基金对中国大陆创作者）未说明——**对国内落地是关键约束**。
  - **版权风险**：@CrazyKaomei 自曝的剪纸风 Skill 使用 5 个知名 IP 形象；"邵氏画风"的风格模仿与厂标使用边界。
  - **`moxt` 全部信息待核实**（原文未做任何说明）。
  - **`doubao` 未做网络检索核实**；开发方归属、模型档位对应关系、免费额度均未证实。
  - 本批第 3 篇的**往期 5 篇同系列文章未入库、未阅读**，其数据本库均未采信。
  - 本批第 2 篇**原文正文存在明显的中英文重复段落**（多处一节内容出现两遍），疑为原文排版/机翻叠加，来源页按语义去重并已标注。

---

## 2026-09-15（网络检索核实 · Replicate 与 fal）

- **日期**：2026-09-15
- **资料来源**：网络检索（WebSearch），非 Raw 层文件
- **新建页面**：
  - `wiki/entities/replicate.md`（实体）
  - `wiki/entities/fal.md`（实体）
- **确认结论**：
  - **Replicate**：2020 年成立的**开源模型托管 / 推理 API 平台**，~200 模型，**支持自定义模型托管**，按 GPU 计算秒数计费（$0.0002–0.0012/秒），$5 免费额度；文档与社区优于 fal。
  - **fal.ai**：2023 年成立的**生成式媒体模型聚合 API 平台**，**985 endpoints**（图像 406 / 视频 450 / 音频 59 / 3D 35 / 语音 35），按输出计价，$10 免费额度；第三方称其图像 API 份额 50%、视频 44%。
  - 两者在来源文章中的角色一致：**"agent 通过 replicate 或 fal 来生成，看你给了它哪个的 key"**——模型供给依赖执行时配置的 key，与 [[skill文件]] 的"流程与执行器解耦"同构。
- **重要核实发现（模型名存疑）**：来源文章称"目前 **gpt image 2.5** 是最好的图像模型，**seedance 2.5** 是最好的视频模型"。检索到的对应版本为 **GPT Image 1.5** 与 **Seedance 2.0**（字节跳动，2026-02 发布），**两个 "2.5" 版本名均未获证实**，已标注"不排除作者笔误/版本表述误差"。
- **保留分歧（分歧并存）**：**成本优劣并非单向**——多数第三方向对比称 fal 便宜 30–50%，但 tokenmix 测算指出 Replicate 在低硬件档模型（Flux Dev / SDXL）上可能更省（按实际计算秒数计费），成因是 GPU 档位差异；两种说法的**适用范围不同**，已并列保留。
- **待人工确认**：
  - "gpt image 2.5 / seedance 2.5" 两个版本名。
  - 模型数量、价格、市场份额均为第三方 2026 快照，非官方页面；该领域迭代极快（如 Sora 2 API 已关停），需以官网为准。
  - 来源文章未指明其在两个平台上实际调用的模型。

---

## 2026-09-15（增量维护 · 第 7 批）

- **日期**：2026-09-15
- **资料来源**（`raw/articles/`，1 篇未维护文章）：
  1. `Pi Agent 作者 Armin Ronacher 谈 agent 未来：九条反直觉判断.md`（摘录整理 @Justin1024go，2026-09-14 发布；原访谈为 YouTube 视频）
- **新建页面**：
  - 来源摘要（1）：`wiki/sources/armin-ronacher-九条反直觉判断.md`
  - 概念（2）：`wiki/concepts/harness-极简主义.md`、`wiki/concepts/可内省性.md`
  - 实体（4）：`wiki/entities/armin-ronacher.md`、`pi-agent.md`、`earendil.md`、`justin-1024go.md`
- **更新页面**：
  - `index.md`（目录概览新增 8 条，updated 改为 2026-09-15）
  - `wiki/topics/agent工程.md`（**新增「两条工程路线（分歧并存）」**；知识地图加"框架路线""人的位置"两行；相关页面与来源扩充）
- **重要核实发现（标题不准确）**：原文标题称 Armin Ronacher 为"**Pi Agent 作者**"。检索确认 **Pi 的原创作者是 Mario Zechner（libGDX 作者）**，2026-04 由 Earendil 收购后由 Zechner、Ronacher、Colin 共同主导；Ronacher 是**核心使用者与维护者**。已在来源页与实体页**并列标注该分歧**，未直接采信原文标题。
  - 补充核实：Ronacher = Flask / Jinja 作者，Pygments / Sphinx / Werkzeug / Click 贡献者，Sentry 十年（2025-03 离开），2025 年与 Colin Daymond Hanna 创立 **Earendil**（公益公司）；Pi 为 TypeScript + MIT，约 80,000+ stars（第三方快照，各来源数字不一）。
- **保留分歧（分歧并存，本批核心贡献）**：本库首次记录**两组明确的 agent 工程路线对立**：
  1. **事后治理派 vs 事前极简派**：@coder-left 深入 Claude Code 的上下文压缩/裁剪机制（[[上下文压缩]]）vs Ronacher 主张框架极简、从源头避免膨胀（[[harness-极简主义]]）。**共识**是"上下文是稀缺资源"，**分歧**在解法。已在 `agent工程.md` 以对照表并列保留。
  2. **全功能 harness vs 极简 harness**：Claude Code（系统提示约 7,000–10,000 tokens、预置 sub-agents / hooks / MCP）vs Pi（< 1,000 tokens、四工具、无内置沙箱需自建容器）。各有代价，未取舍。
- **新增维度**：[[可内省性]]——Ronacher 提出"机器不可问责，所以人类不会退场"、"Markdown / JSON / Unix 管道在赢，因为人能看懂"，与既有的 [[审批门]] 互补（审批门解决"能不能拦住"，可内省性解决"人是否理解发生了什么"）。
- **待人工确认**：
  - 摘录者 @Justin1024go 身份；原访谈视频（YouTube）**未逐字核对**，九条内容为二手转述。
  - Pi 的 star 数各来源不一（58,000 / 80,000+ / 85,000）；收购日期有 2026-04-08 与 2026-05 两种说法。
  - "全功能 harness 系统提示 7,000–10,000 tokens"为第三方口径，未逐项核对。
  - Earendil 的融资、估值、员工数未披露；名称有 "Earendil Inc." / "Earendil Works" 两种表述；Lefos 信息有限未建页。
  - 第 07 条"Earendil 是唯一没有自动修 issue 机器人的 harness 公司"为自嘲式表述，未核实。
  - 两条工程路线均**无对照评测数据**。

---

_（新记录追加在下方，日期倒序）_
