---
title: Obsidian Sync via Git
created: 2026-06-30
updated: 2026-06-30
type: concept
tags: [obsidian, git, workflow, markdown, tutorial]
sources: [raw/articles/obsidian-basics-git-sync-2026-06-30.md, raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md, raw/articles/karpathy-llm-wiki-2026-04-13.md]
confidence: medium
contested: false
contradictions: []
---

# Obsidian Sync via Git

Obsidian Sync via Git 指的是不依赖官方付费同步，而是用 Git 仓库、远程代码托管和插件/命令行完成笔记同步、备份与版本管理。对于希望低成本搭建第二大脑或 LLM Wiki 的用户，这是常见起步方案。 ^[raw/articles/obsidian-basics-git-sync-2026-06-30.md] ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md]

## 常见流程

1. 创建或初始化本地 vault 仓库。
2. 配置 `.gitignore`，忽略 workspace 等临时状态文件。
3. 连接远程仓库并定期 push / pull。
4. 可选安装 Obsidian Git 等插件以自动同步。 ^[raw/articles/obsidian-basics-git-sync-2026-06-30.md] ^[raw/articles/karpathy-llm-wiki-2026-04-13.md]

## 为什么重要

- 免费或低成本。
- 版本可回滚，适合 AI 批量修改文件后的安全兜底。
- 让 [[obsidian]] 与 [[llm-wiki]] 保持本地优先，同时获得异地备份能力。 ^[raw/articles/youtube-obsidian-second-brain-tutorial-2026-06-30.md] ^[raw/articles/karpathy-llm-wiki-2026-04-13.md]

## 相关

- [[obsidian]]
- [[llm-wiki]]
- [[source-ingestion-workflow]]
