---
title: Source Ingestion Workflow
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [workflow, automation, markdown, obsidian, knowledge-base]
sources: [raw/articles/karpathy-llm-wiki-2026-04-13.md]
confidence: medium
contested: false
contradictions: []
---

# Source Ingestion Workflow

资料摄入是 [[llm-wiki]] 能持续增长的入口。标准流程是：先保存原始资料，再由 AI 更新概念页、实体页、索引和日志。

## 推荐流程

1. 用 Obsidian Web Clipper、手动复制、PDF 提取或脚本把资料保存到 `raw/`。
2. 为 raw 文件添加 frontmatter：`source_url`、`ingested`、`sha256`。
3. AI 阅读原始资料，提取核心实体、概念、流程、争议点。
4. 检查 `index.md` 和现有页面，避免重复创建页面。
5. 创建或更新 `concepts/`、`entities/`、`comparisons/` 中的页面。
6. 更新 `index.md` 的页面清单和摘要。
7. 在 `log.md` 记录本次动作。

## Obsidian 配置建议

- 启用 Obsidian 双链，让页面引用可点击。
- 图片尽量本地化，避免外链失效。
- 可以使用 Graph View 检查孤岛页面和缺失链接。
- 可选安装 Dataview，但当前阶段 `index.md` 已足够。
- 建议用 Git 或 Obsidian Git 插件保存版本历史。

## 相关

- [[llm-wiki]]
- [[obsidian]]
- [[rag-vs-llm-wiki]]
