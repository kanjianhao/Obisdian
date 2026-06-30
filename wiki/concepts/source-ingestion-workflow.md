---
title: Source Ingestion Workflow
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [workflow, automation, markdown, obsidian, knowledge-base]
sources: [raw/articles/karpathy-llm-wiki-2026-04-13.md, raw/articles/obsidian-ai-workflows-2026-04-22.md, raw/articles/claude-obsidian-second-brain-2026-04-14.md]
confidence: medium
contested: false
contradictions: []
---

# Source Ingestion Workflow

资料摄入是 [[llm-wiki]] 能持续增长的入口。标准流程是：先保存原始资料，再由 AI 更新概念页、实体页、索引和日志。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md] ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md]

## 推荐流程

1. 用 Obsidian Web Clipper、手动复制、PDF 提取或脚本把资料保存到 `raw/`。
2. 为 raw 文件添加 frontmatter：`source_url`、`ingested`、`sha256`。
3. AI 阅读原始资料，提取核心实体、概念、流程、争议点。
4. 检查 `index.md` 和现有页面，避免重复创建页面。
5. 创建或更新 `concepts/`、`entities/`、`comparisons/` 中的页面。
6. 更新 `index.md` 的页面清单和摘要。
7. 在 `log.md` 记录本次动作。

## 常见入口

- 网页文章：Obsidian Web Clipper 剪藏后进入 `raw/articles/`。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md] ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 已读高亮和外部知识流：可通过 Readwise、Weread 等同步到 vault，再进入整理流程。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- 会议录音：先转录，再整理成纪要和待办。文中提到使用 Whisper 本地转写。 ^[raw/articles/obsidian-ai-workflows-2026-04-22.md]
- URL / PDF / transcript：有些 LLM Wiki 工具会直接把这些来源交给 AI 代理完成 ingest。 ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md]

## Obsidian 配置建议

- 启用 Obsidian 双链，让页面引用可点击。
- 图片尽量本地化，避免外链失效。
- 可以使用 Graph View 检查孤岛页面和缺失链接。
- 可选安装 Dataview，但当前阶段 `index.md` 已足够。
- 建议用 Git 或 Obsidian Git 插件保存版本历史。 ^[raw/articles/karpathy-llm-wiki-2026-04-13.md] ^[raw/articles/obsidian-ai-workflows-2026-04-22.md] ^[raw/articles/claude-obsidian-second-brain-2026-04-14.md]

## 相关

- [[llm-wiki]]
- [[obsidian]]
- [[obsidian-ai-workflows]]
