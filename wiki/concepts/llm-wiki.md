---
title: LLM Wiki
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [llm, wiki, knowledge-base, obsidian, workflow]
sources: [raw/articles/karpathy-llm-wiki-2026-04-13.md, raw/articles/claude-obsidian-second-brain-2026-04-14.md, raw/articles/obsidian-ai-workflows-2026-04-22.md]
confidence: medium
contested: false
contradictions: []
---

# LLM Wiki

LLM Wiki 是一种由 AI 增量维护的持久化知识库：资料先被保存为不可变原始来源，然后由 AI 提炼成互相链接的 Markdown 页面。它的核心目标是让知识不断沉淀，而不是每次提问都重新检索、重新拼接。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md] ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md]

## 核心思想

- 人负责选择素材、提出问题、判断方向。
- AI 负责整理、摘要、建链接、更新索引、发现矛盾。
- 知识以普通 Markdown 文件保存，适合放在 [[obsidian]] 里查看和编辑。
- 通过 Obsidian 双链语法让概念之间形成图谱，而不是孤立笔记。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md]

## 常见实现形态

一种实现方式是把 vault 组织为 raw sources、concepts、entities、index 和 log，然后通过 ingest/query/lint 这样的流程持续维护。另一种实现方式是用专门插件或命令，把资料丢入 vault 后由 AI 自动生成结构化页面和交叉引用。重点不在具体工具，而在“知识要持续编译成 wiki，而不是仅在查询时临时搜索”。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md] ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md] ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]

## 与 RAG 的关键区别

[[rag-vs-llm-wiki]] 的差异在于：RAG 常常是在每次查询时临时检索片段；LLM Wiki 则把理解和整理工作提前沉淀到页面里，后续查询直接基于已整理的知识网络。

## 本仓库的使用方式

1. 新资料进入 `raw/`，保持原样。
2. 重要概念进入 `concepts/`，工具/平台/人物进入 `entities/`。
3. 对比和决策类内容进入 `comparisons/`。
4. 值得复用的问题答案进入 `queries/`。
5. 每次更新都维护 `index.md` 和 `log.md`。

## 相关

- [[source-ingestion-workflow]]
- [[obsidian]]
- [[rag-vs-llm-wiki]]
- [[claude-obsidian]]
