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
updated: 2026-09-14
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

_（新记录追加在下方，日期倒序）_
