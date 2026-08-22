---
title: "AI 写作去味"
type: topic
aliases:
  - "去 AI 味工作流"
  - "去AI味实战"
  - "AI 写作"
  - "文风塑造"
tags:
  - topic
  - AI写作
  - 去AI味
sources:
  - "[[去ai味完整实战教程]]"
created: 2026-08-17
updated: 2026-08-17
---

# AI 写作去味

## 摘要

「AI 写作去味」是围绕 [[去ai味|去 AI 味]] 的一套完整方法论与工具生态：先厘清 AI 味是什么，再用分层的 Skill 组合（清理套路 → 中文重写 → 说人话 → 建立文风 → 提取思维）把 AI 初稿改造成自然、具体、带作者个人信息的文字。其终点不是骗过 AI 检测器，而是**增加作者信息密度**。

## 核心内容

### Skill 全景分类

| 类别 | 项目 | 解决的问题 | 是否单独建页 |
| --- | --- | --- | --- |
| AI 文本检测（研究） | ChatGPT-Comparison-Detection、AIGC_text_detector | 判断文字更可能来自人还是 AI | 否（信息少） |
| 清理 AI 套路 | [[stop-slop]]（含 stop-slop-zh） | 清理 AI 高频写作坏习惯 | 是 |
| 中文 AI 腔改写 | [[humanizer-zh]]、qu-ai-wei | 把 AI 初稿改得像正常中文 | humanizer-zh 建页 |
| 场景化表达 | [[shuorenhua]] | 按真实场景切换表达 | 是 |
| 整体去 AI 化 | ai-flavor-remover、De-AI-Prompt-Enhancer | 一次性整体去味 / 把规则固化为 Skill | 否 |
| 建立个人文风 | [[writing-style-skill]]、WRITING.md | 让 AI 写得像我 | 是 |
| 技术写作规范 | [[agent-style]] | 英文技术写作规则（21 条） | 是 |
| 思维框架提取 | [[nuwa-skill]] | 提取判断方式与思维模型 | 是 |
| 学术/MBA 论文 | humanize-mba-text-skill | 论文去味（保持正式严谨） | 否 |
| 网络小说 | oh-story-claudecode | 网文去味（人物/节奏/悬念） | 否 |
| 内容生产系统 | AIWriteX | 批量内容流水线（热点→发布） | 否 |
| 前端/UI 审美 | taste-skill | AI 前端 UI 去同质化（**非文章去味**） | 否 |

### 未单独建页项目的仓库地址（已检索核实）

| 项目 | 仓库地址 | 备注 |
| --- | --- | --- |
| qu-ai-wei | https://github.com/LifelongLazyLearner/qu-ai-wei | 简体中文去味，MIT，v0.9.x，支持 Codex/Claude Code/Kimi Code/Cursor |
| ai-flavor-remover | https://github.com/hylarucoder/ai-flavor-remover | 中文长文本去味 Prompt，作者主要在 Gemini 2.5 Pro 测试 |
| De-AI-Prompt-Enhancer | https://github.com/OUBIGFA/De-AI-Prompt-Enhancer-Writer-Booster-SKILL | good-writing + de-AI-writing 双模式，含 24 项痕迹检测 |
| humanize-mba-text-skill | https://github.com/stephenlzc/humanize-mba-text-skill | 中文 MBA 论文，Python 检测+改写，v1.4.0，支持 Claude Code/Kimi CLI |
| oh-story-claudecode | https://github.com/worldwonderer/oh-story-claudecode | 网文写作，覆盖扫榜/拆文/写作/去味/封面 |
| AIWriteX | https://github.com/iniwap/AIWriteX | 公众号内容生产工作流（热点→选题→生成→排版→发布） |
| taste-skill | https://github.com/leonxlnx/taste-skill | 前端/UI 审美，非文章去味（~21k stars） |
| ChatGPT-Comparison-Detection | https://github.com/Hello-SimpleAI/chatgpt-comparison-detection | HC3 数据集 + 检测研究 |
| AIGC_text_detector | https://github.com/YuchuanTian/AIGC_text_detector | ICLR 2024 Spotlight 论文对应检测代码 |

### 四层选择法（中文创作者）

1. **第一层 · 去掉最明显 AI 腔**：stop-slop-zh / [[humanizer-zh]] / qu-ai-wei → 别让文章一眼 AI。
2. **第二层 · 说人话**：[[shuorenhua]] → 别只写正确的话，要写自然的话。
3. **第三层 · 建立文风**：[[writing-style-skill]] / WRITING.md → 不要只像真人，要像你。
4. **第四层 · 建立思维系统**：[[nuwa-skill]] → 不仅模仿语言，还模仿你的判断方式。

### 推荐工作流（6 步）

1. **AI 做资料和第一稿**（解决事实/资料/逻辑/结构，不要一开始就疯狂限制）。
2. **AI 腔检查**（stop-slop-zh 或自己的 WRITING.md，找套话/废话/机械排比/强行总结）。
3. **中文重写**（[[humanizer-zh]] / qu-ai-wei / [[shuorenhua]]；**绝对不能虚构经历**）。
4. **加入只有你知道的信息**（用了几天、哪里失败、花多少钱、客户抱怨什么）——最重要的一步。
5. **writing-style-skill 统一文风**（个人规则：短句为主、不凑三点、少写"不是…而是…"）。
6. **从修改中持续学习**（AI 写 → 你改 → 比较差异 → 提取规则 → 更新 Skill）。

### 发布前 7 项自检

1. 开头能不能直接删掉一段？
2. 有没有连续模板化排比？
3. 有没有一句话说了等于没说？
4. 有没有为了真人感编造经历？
5. 有没有真正属于作者自己的判断？
6. 有没有具体事实、数据、案例或使用细节？
7. 这句话念出来会不会别扭？

### 关键结论

- 去 AI 味的终点**不是骗过 AI Detector**，而是往文章里放入别人没有的东西：经历、判断、数据、失败、观察、审美、表达方式。
- 各工具分工：stop-slop 删套路 → humanizer-zh 恢复自然中文 → shuorenhua 场景化 → writing-style-skill 学习你的语言 → nuwa-skill 提取思维方式。最终决定文章是不是你的，依然是你自己提供的信息和判断。

## 相关页面

- 概念：[[去ai味]]
- 实体：[[stop-slop]]、[[humanizer-zh]]、[[shuorenhua]]、[[writing-style-skill]]、[[nuwa-skill]]、[[agent-style]]
- 来源：[[去ai味完整实战教程]]

## 来源与待核实问题

- 来源：[[去ai味完整实战教程]]
- ✅ 已核实：表格中未单独建页的项目仓库地址均已在「未单独建页项目的仓库地址」表中列出（网络检索）。
- ✅ 已确定（按社区口碑 star 数）：三个同名多仓库 Skill 的主推版本如下（均支持 Claude Code）——
  - stop-slop-zh → `pencil20388-eng/stop-slop-zh`（41 stars 最高）
  - Humanizer-zh → `op7418/Humanizer-zh`（15481 stars 绝对领先）
  - shuorenhua → `MrGeDiao/shuorenhua`（1098 stars、仍在活跃维护）
