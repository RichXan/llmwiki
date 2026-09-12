---
title: "从 intent.md 到闭环：AI 原生软件开发（Anthropic 手册解读）"
type: source
aliases:
  - "从 intent 到闭环"
  - "AI 原生 SDLC 手册解读"
  - "The AI-Native SDLC playbook"
tags:
  - source
  - article
  - AI原生
  - 软件工程
  - SDLC
sources:
  - "[[raw/articles/从 intent.md 到闭环：AI 原生软件开发的六个阶段、一条产物链、几道审批门 原创]]"
created: 2026-09-12
updated: 2026-09-12
---

# 来源摘要：从 intent.md 到闭环

## 摘要

本文是作者（X：@shao__meng）对 Anthropic 官方文章《[The AI-Native SDLC playbook](https://claude.com/blog/the-ai-native-sdlc-playbook)》（作者 [[louis-claxton|Louis Claxton]]，Anthropic Applied AI 团队，2026-08-21 发布）的中文解读。原文把 Anthropic 在企业客户落地 Claude Code 的经验，按软件开发生命周期拆成六个阶段（Plan / Design / Build / Test / Deploy / Maintain），每个阶段以提交一份**产物**结束，并以**审批门**约束 Agent。解读逐节梳理了论证、做法与隐含假设，最后给出作者自己的评价与适用范围。

## 元信息

- **原文**：《The AI-Native SDLC playbook》，作者 Louis Claxton（Anthropic Applied AI 团队），2026-08-21，https://claude.com/blog/the-ai-native-sdlc-playbook
- **解读作者**：[@shao__meng](https://x.com/shao__meng)
- **发布日期**：2026-09-02
- **原始链接**：https://x.com/shao__meng/status/2095034431614677320
- **原始文件**：`[[raw/articles/从 intent.md 到闭环：AI 原生软件开发的六个阶段、一条产物链、几道审批门 原创]]`
- **入库日期**：2026-09-12

## 核心内容

### 一、问题出在流程，不在代码

- 传统 SDLC 之所以每步设文档、签字、会议，是因为它诞生在**写代码最贵、最慢的年代**，且默认每一步都由人执行。当构建阶段从几周压缩到几小时，出现三个后果：**瓶颈转移**（计划/评审/部署仍按人的速度）、**控制手段与现实脱节**（逐行审查跟不上 agent 产出的大量 diff）、**治理成本上升**。
- 结论：实现阶段的变革程度，整个 SDLC 都要经历同等变革。详见 [[ai原生sdlc]]。

### 二、AI 原生 SDLC 的三个机制

1. **流程从线性变成循环**：维护阶段发现的问题写成新的 intent，重新进入计划阶段。
2. **每个阶段以提交一个产物结束**：`intent.md`(Plan) → `spec.md`(Design) → `plan.md`+diff+测试(Build) → 测试输出+CI(Test) → 带评审记录的 PR(Deploy) → 事故记录→新 intent(Maintain)。这条提交链本身就是**审计轨迹**。详见 [[产物链]]。
3. **人的注意力集中在门上**：产物被接受即触发下一阶段，人只在门口审阅 agent 标记的问题。详见 [[审批门]]。

### 三、六个阶段（每个 play 统一结构：改变了什么 / 前置条件 / 基础设施 / 执行步骤 / 治理考量 / 领先与滞后指标）

- **Stage 1 · 计划**：让发起人直接和 Claude 讨论、用自己的话写成 `intent.md`（要什么、为什么、约束、影响、未想清楚的问题）；非工程师经 claude.ai / Cowork 通过 GitHub connector 提交。领先指标是从首次对话到 intent 提交的时间；滞后指标是接受率与 intent 被改次数。
- **Stage 2 · 设计**：Claude 读取已接受的 intent，在品牌/安全/合规/UX skill 约束下**一次产出需求与设计规格**并标出问题，产品负责人**只审不写**。演进路径：手动 prompt → 组织级 slash command → 合并 intent 自动触发以 PR 提交 spec。
- **Stage 3 · 构建**（六个 play，篇幅最长）：plan mode 为默认起点（计划未通过则不能改文件）；auto mode 在护栏成熟后成为日常默认（从逐条审转为审阅产物）；遗留系统三种配置（仓库为事实来源 / 遗留系统为事实来源 / 双向链接）；`CLAUDE.md` 保持一页以内；Skill 是**建议性控制**；hook 作为构建期护栏且**不放人工审批**；并行会话 vs 子代理。
- **Stage 4 · 测试**：给 Claude 反馈回路（单命令验证、目标可量化、**修 bug 先写失败测试**、用 hook 阻止修改测试文件）；CI 中的 eval 套件（20–50 个真实任务，配置变更时运行，事故转为 eval）。详见 [[eval-套件]]。
- **Stage 5 · 部署**：**agent 可以完成生产门之前的一切工作，但不能跨过这道门**。AI 进入 PR 评审（`REVIEW.md` 分 pass，职责分离靠"写代码的 agent 无批准途径"）；hook 作为审批门；受监管企业的托管设置（`permissions.deny/allow`、`disableBypassPermissionsMode`、sandbox、`failIfUnavailable`、凭据、`allowManagedHooksOnly`、`requiredMinimumVersion` 等）；CI/CD 集成（只读判断 → 门后写操作）；回滚应是演练最多的路径。
- **Stage 6 · 维护（闭环）**：**确定性脚本**监控生产指标（滚动均值 + 标准差 + Western Electric 规则），按 `bands.yaml` 分级响应（1σ 记日志 / 2σ 只读诊断 / 3σ 可行动但只能开 PR 或触发预批准 runbook）；Claude 把诊断写成 intent 回到正常流程；定期代码库扫描（Claude Security）；Claude Tag 在 Slack 事故频道值班。

### 四、贯穿全文的设计原则

- 建议性控制（Skill/CLAUDE.md/prompt）与确定性控制（hook/沙箱/分支保护/托管设置）分两层。
- 检测用确定性脚本，响应分级，行动受门约束。
- Agent 不能批准自己的工作，也不能削弱对自己工作的检查。
- 引导 agent 的配置（CLAUDE.md、skill、hook、REVIEW.md）与代码同等对待，进 git、走 review、跑 eval。
- 度量来自已有系统（git 时间戳、PR 元数据、CI 日志、OpenTelemetry、事故追踪器）。
- 人不在并行会话的关键路径上。

### 五、解读作者的评价

- **长处**：正面回答受监管企业关心的问责、审计、职责分离、变更管理问题；演进路径务实（先手动→固化命令→自动触发），承认遗留系统不会消失。
- **需留意**：这是一篇产品文章，落地细节绑定 Claude 生态（Claude Security、Claude Tag 尚在公测且限 Enterprise）；前置条件不轻（依赖单命令测试套件、可靠构建、成熟 CI/CD）；人的评审是隐含上限；eval 维护成本可能被低估；从 intent 到 spec 的自动化对产品组织要求高。
- **适用范围**：适合已在用 agentic 编码工具、感到流程跟不上代码的中大型组织（尤其受监管行业）；小团队可只取几个 play（plan mode、CLAUDE.md、反馈回路、AI 评审）。

## 相关页面

- 概念：[[ai原生sdlc]]、[[意图文件]]、[[产物链]]、[[审批门]]、[[建议性控制与确定性控制]]、[[eval-套件]]、[[agent-loop]]
- 实体：[[anthropic]]、[[claude-code]]、[[louis-claxton]]、[[shao-meng]]
- 主题：[[ai原生软件开发]]、[[agent工程]]

## 来源与待核实问题

- **来源**：https://x.com/shao__meng/status/2095034431614677320（原文 https://claude.com/blog/the-ai-native-sdlc-playbook）
- **待核实**：
  - 本文为中文解读，个别表格（如产物链、托管设置）在原 t.co 剪藏中因排版丢失，本摘要依据正文文字还原，未与原英文 PDF 逐字校对。
  - 解读作者 @shao__meng 的身份、以及文中提到的 Claude Security / Claude Tag / Cowork 的正式发布状态与定价。
  - 原文提到的具体指标数值（如 intent 提交时间"从几周降到几小时"）为作者预期，非实测结论。
