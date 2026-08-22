---
title: "claude-obsidian"
type: entity
aliases:
  - "claude obsidian 插件"
  - "Claude + Obsidian knowledge companion"
tags:
  - entity
  - 工具
  - 开源项目
  - ClaudeCode插件
sources:
  - "[[codex-obsidian-自生长个人知识库]]"
  - "https://github.com/AgriciDaniel/claude-obsidian"
  - "https://claudewave.com/repo/agricidaniel-claude-obsidian"
created: 2026-08-17
updated: 2026-08-17
---

# claude-obsidian

## 摘要

claude-obsidian 是一个基于 [[karpathy|Karpathy]] LLM Wiki pattern 的 Claude Code 插件（GitHub：[AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian)，MIT 协议），定位「Claude + Obsidian knowledge companion」。它把知识库的摄入、检索、维护封装成 15 个结构化 skill，让一个 Obsidian Vault 变成自组织的、会持续复利增长的知识库。在 [[自生长个人知识库]] 文章中，它对应**方式二**。

## 核心内容

### 核心理念

围绕一条可复用的循环组织：**保留来源（retain）→ 溯源声明（ground）→ 连接知识（connect）→ 复用（put back to work）**。Vault 始终是普通的 Markdown/JSON 目录，不被锁进插件缓存或云数据库，用户拥有文件主权。

### 15 个 skill（按用途）

- **构建与使用**：`wiki`（初始化/接管 vault）、`save`（保存单个答案，非自动转写）、`wiki-ingest`（来源→链接页面+溯源记录）、`wiki-query`（基于证据回答）、`wiki-lint`（死链/孤立页/元数据缺失/空章节检查）。
- **扩展工作流**：`autoresearch`（有界网络研究）、`canvas`（Obsidian Canvas 创建维护）、`defuddle`（入库前清洗网页）、`wiki-fold`（操作日志可追溯回滚）、`wiki-mode`（Generic/LYT/PARA/Zettelkasten 归档约定）、`wiki-retrieve`（上下文前缀 + BM25 + 余弦重排检索）、`wiki-cli`（事务安全读写）。
- **参考**：`obsidian-markdown`（正确 OFM 语法）、`obsidian-bases`（.base 表格）、`think`（observe/listen/connect/create/grow 循环）。

### 常用命令

- `/wiki`：初始化、诊断、继续上次进度。
- `ingest [file]`：读取来源 → 创建 8–15 个 wiki 页 → 更新索引与日志；`ingest all of these` 批量处理。
- `/save [name]`、`/autoresearch [topic]`、`/canvas`、`lint`、`update hot cache`。

### 检索机制

采用混合检索栈：上下文前缀搜索 + BM25 + 余弦重排（基于 Anthropic 2024 年 9 月的 contextual retrieval 研究）。

### 安装方式（三种）

1. **Clone as vault（推荐）**：`git clone` 后运行 `bash bin/setup-vault.sh`，2 分钟完成预配置（图谱配色、目录结构）。
2. **作为 Claude Code 插件**：`claude plugin marketplace add AgriciDaniel/claude-obsidian` → `claude plugin install claude-obsidian@claude-obsidian-marketplace`。
3. **加入现有 Vault**：复制 `WIKI.md` 到 Vault 根目录，按提示初始化。

### 多 Agent 支持

- 支持 Claude Code、Codex、OpenCode、Gemini 等多 host（`bin/setup-multi-agent.sh --host codex`）。

### 局限（相对方式三 [[wesight]]）

- 主要操作仍在外部 Agent 工具中，需理解并调用 ingest / retrieve 等指令。
- Obsidian 更多承担文件存储与结果浏览，任务状态、执行过程与知识变化缺少直观可视化反馈。
- 对首次接触该架构的用户，使用门槛依然存在。

## 相关页面

- 工具：[[wesight]]、[[obsidian]]、[[workbuddy]]、[[codex]]
- 人物：[[karpathy]]
- 概念：[[llm-wiki]]、[[llm-wiki-三层架构]]
- 主题：[[自生长个人知识库]]
- 来源：[[codex-obsidian-自生长个人知识库]]

## 来源与待核实问题

- 来源：
  - [[codex-obsidian-自生长个人知识库]]（方式二简介）
  - https://github.com/AgriciDaniel/claude-obsidian （项目仓库）
  - https://claudewave.com/repo/agricidaniel-claude-obsidian （Trust 100/100、版本历史）
- 待核实：
  - GitHub 上存在多个同名/相关仓库（`AgriciDaniel`、`LabinatorSolutions`、`alexdemenezes`），主体与 fork 关系**待核实**。
  - 文中未给出仓库链接，本文以 `AgriciDaniel/claude-obsidian` 为准，其余同名仓库需人工确认。
  - skill 数量、版本号（v1.7/v1.8/v1.9）随版本迭代，以仓库最新 README 为准。
