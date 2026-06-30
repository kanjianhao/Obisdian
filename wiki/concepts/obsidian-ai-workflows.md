---
title: Obsidian AI Workflows
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [obsidian, workflow, automation, ai, note-taking]
sources: [raw/articles/obsidian-ai-workflows-2026-04-22.md, raw/articles/hermes-agent-guide-2026-04-15.md, raw/articles/claude-obsidian-second-brain-2026-04-14.md, raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md, raw/articles/obsidian-basics-git-sync-2026-06-30.md]
confidence: medium
contested: false
contradictions: []
---

# Obsidian AI Workflows

Obsidian AI Workflows 指的是把 Obsidian 从“记笔记的软件”扩展成“资料、流程模板、历史结果和 AI 代理协作的工作台”。在这种模式下，信息输入、汇聚、处理、维护和输出都围绕同一个 vault 展开。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md] ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]

## 常见流程环节

- 输入：网页剪藏、手机输入、语音/图片/聊天入口。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 汇聚：把日历、待办、记账或其他外部数据汇入每日笔记。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 处理：月报草稿、会议纪要、读书笔记转内容大纲。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 维护：扫描孤儿笔记、补充链接、批量改标签和 YAML 属性。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 输出：把成稿排版后发往外部渠道。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]

## 面向新手的落地路径

- 先完成 [[obsidian]] 安装、基础设置、Markdown 入门和双向链接理解。 ^[raw/articles/obsidian-basics-git-sync-2026-06-30.md] ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]
- 再接入 Git、同步、CLI 和 Web Clipper 这类基础设施。 ^[raw/articles/obsidian-basics-git-sync-2026-06-30.md] ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]
- 最后才是把 [[claude-code]]、[[hermes-agent]] 或其他 Agent 工具接进来做自动整理与生成。 ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]

## 为什么适合放在 Obsidian

- 工作流说明、模板、配置和结果都能落在本地 Markdown 文件里。
- 可替换底层 AI 工具，而不丢失历史资料和流程定义。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 既能和 [[hermes-agent]] 这类通用 Agent 配合，也能与 [[claude-obsidian]] 这类围绕 vault 的专门方案配合。

## 与 LLM Wiki 的关系

[[llm-wiki]] 偏重知识沉淀；Obsidian AI Workflows 的范围更大，除了知识页，还包括自动写月报、处理会议纪要、发布内容等生产流程。因此它可以把知识库视为其中一个核心子系统。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md] ^[raw/articles/hermes-agent-guide-2026-04-15.md] ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md] ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]

## 相关

- [[obsidian]]
- [[llm-wiki]]
- [[source-ingestion-workflow]]
- [[hermes-agent]]
- [[claude-obsidian]]
- [[obsidian-sync-via-git]]
