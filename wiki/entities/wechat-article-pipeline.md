---
title: "wechat-article-pipeline"
type: entity
aliases:
  - "公众号排版流水线"
  - "wechat article pipeline"
  - "微信公众号排版"
tags:
  - entity
  - 工具
  - 公众号排版
  - 开源项目
sources:
  - "[[手调半小时的公众号排版]]"
  - "https://github.com/davinci-seven/wechat-article-pipeline"
created: 2026-08-18
updated: 2026-08-18
---

# wechat-article-pipeline

## 摘要

wechat-article-pipeline 是 [[davinci-seven|达芬七]] 开源的公众号排版流水线（GitHub：davinci-seven/wechat-article-pipeline，MIT 协议）。它把定稿 Markdown + 配图放进一个文件夹，跑一条命令，产出可直接粘贴到公众号后台的排版——作者实测 3864 字、5 张图耗时 25 秒。

## 核心内容

### 用法

```powershell
.\tools\公众号排版.ps1 -ArticleDir .\我的文章 -OpenPreview
# 换主题
.\tools\公众号排版.ps1 -ArticleDir .\我的文章 -Theme red-white
```

- 也可把文章文件夹直接拖到 `公众号排版.bat` 上。
- 浏览器弹出预览页，点绿色按钮复制，到公众号后台 Ctrl+V 即可。

### 六套主题

橄榄手记（深度评测/案例复盘）、摸鱼绿（教程/工具盘点）、红白色系（观点文）、石墨极简（科技/设计）、留白禅意（随笔）、摸鱼票据（工具对比）。同一篇稿子换参数重跑即可切换。

### 四样产出

1. **预览页**：带绿色复制按钮，用来复制。
2. **发布稳定版**：图片全部内嵌进 HTML，不依赖本机路径，可换电脑/发给别人/长期保存。
3. **390px 手机长截图**：发前预览读者手机端效果。
4. **检查报告**：原稿哈希、HTML 合规校验、隐私扫描、图片证据表（每张图的顺序/路径/章节/图注）。

### 三条底线（不做的事）

- 不改原稿、不替你发布、图片少一张就停下来报错。
- 跑之前跑完各算一次 SHA256，对不上直接中止。

### 工程踩坑（作者自述，体现"表面成功≠真实成功"）

- 长截图曾"假装成功"（只检查文件存在、实际无人生成）→ 重接 Playwright，以 390px 视口真实截图、长文分段拼接。
- 隐私检查曾报"0 ERROR"却已泄露本机绝对路径：根因是 PowerShell 5.1 的 `Tee-Object` 默认写 UTF-16LE，脱敏脚本按 UTF-8 读成乱码 → 重写为显式 UTF-8 + 按 BOM 识别编码。
- 外部代码审核发现渲染器遇不支持语法不报错（引用块/斜体/删除线符号原样显示、列表格式被剥、句中图片消失）→ 补齐语法，仍不支持的命中即停并报行号/原因。

### 与底层项目的关系

作者明确声明：最难的底层能力不是自己写的，本工具是把三个开源项目"接成一条自己愿意每天用的流水线"，并补上 Windows 一键入口、原稿哈希、图片检查、稳定版 HTML、长截图、隐私检查、Agent 执行规则。详见 [[公众号排版自动化]]。

- [[gzh-design]]：解决公众号编辑器兼容、一键复制、HTML 检查、主题基础。
- [[xiaowan-wechat-layout]]：手机端结构检查、图片证据、排版 QA 思路。
- [[md2wechat]]：公众号素材上传与草稿创建。

## 相关页面

- 作者：[[davinci-seven]]
- 底层：[[gzh-design]]、[[xiaowan-wechat-layout]]、[[md2wechat]]
- 主题：[[公众号排版自动化]]
- 关联工具：[[wesight]]
- 来源：[[手调半小时的公众号排版]]

## 来源与待核实问题

- 来源：[[手调半小时的公众号排版]]、https://github.com/davinci-seven/wechat-article-pipeline
- 待核实：仓库维护状态；六套主题的具体视觉细节。
