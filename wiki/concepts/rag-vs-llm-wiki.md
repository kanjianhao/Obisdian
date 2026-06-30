---
title: RAG vs LLM Wiki
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [rag, llm, wiki, knowledge-base, comparison]
sources: [raw/articles/karpathy-llm-wiki-2026-04-13.md]
confidence: medium
contested: false
contradictions: []
---

# RAG vs LLM Wiki

RAG 和 [[llm-wiki]] 都能帮助 AI 使用外部资料，但它们的知识管理哲学不同。

| 维度 | RAG | LLM Wiki |
|---|---|---|
| 工作方式 | 查询时检索相关片段 | 事先把来源整理成互链页面 |
| 知识积累 | 常常每次从零开始 | 每次处理都会沉淀到知识库 |
| 维护对象 | 向量库、文档切片、检索参数 | Markdown 页面、索引、双链 |
| 适合场景 | 大量文档问答、客服、快速检索 | 长期研究、个人知识管理、复利式理解 |
| 风险 | 检索漏召回、上下文拼接碎片化 | 需要维护 schema、索引和链接 |

## 综合判断

RAG 更像“临时查资料”，LLM Wiki 更像“持续写百科”。如果目标是长期研究和个人知识复利，[[llm-wiki]] 更适合；如果目标是对海量动态文档做一次性问答，RAG 仍然有价值。

## 相关

- [[llm-wiki]]
- [[source-ingestion-workflow]]
- [[obsidian]]
