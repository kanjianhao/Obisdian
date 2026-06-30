# Obsidian LLM Wiki

这是一个运行在 Obsidian vault 里的 LLM Wiki 知识库。

目标不是把资料简单堆进文件夹，而是把笔记、剪藏、教程、AI Agent 工作流和结构化知识页放进同一个可持续维护的 Markdown 仓库里，让 AI 负责整理、交叉引用、更新索引和沉淀长期知识。

当前仓库已经完成：
- Git 仓库初始化
- GitHub 远程仓库连接与推送
- `wiki/` 目录初始化
- 首批 Obsidian / Hermes / LLM Wiki 资料 ingest
- 基础知识页、实体页、对比页与日志建立

## 仓库结构

```text
.
├─ 00 Inbox/                  # 新剪藏、待处理笔记、暂存资料
├─ wiki/
│  ├─ SCHEMA.md               # Wiki 规则、标签体系、页面规范
│  ├─ index.md                # Wiki 总索引
│  ├─ log.md                  # Wiki 变更日志
│  ├─ raw/                    # 原始资料层（不可直接修改）
│  │  ├─ articles/
│  │  ├─ papers/
│  │  ├─ transcripts/
│  │  └─ assets/
│  ├─ entities/               # 实体页：工具、平台、产品、组织等
│  ├─ concepts/               # 概念页：方法论、流程、主题
│  ├─ comparisons/            # 对比页
│  ├─ queries/                # 值得沉淀的问题回答
│  ├─ _meta/
│  └─ _archive/
└─ README.md
```

## Wiki 的工作方式

这个仓库遵循 Karpathy 提出的 LLM Wiki 思路：

1. 先保存 raw source
   - 网页、视频描述、文章、教程先落到 `wiki/raw/`
   - 原始资料保留来源 URL、ingested 日期和 sha256

2. 再抽取结构化知识
   - AI 根据资料更新 `entities/`、`concepts/`、`comparisons/`、`queries/`
   - 页面之间用 `[[wikilinks]]` 建立连接

3. 维护导航与审计线索
   - 每次新增页面都更新 `wiki/index.md`
   - 每次 ingest / update 都记录到 `wiki/log.md`

这样做的好处：
- 保留原始来源，便于回溯
- 知识不是一次性总结，而是可累积、可更新
- Obsidian 可以直接作为浏览器和编辑器使用
- Git 提供历史版本、回滚能力和远程备份

## 当前知识域

目前这个 Wiki 主要覆盖：
- AI / LLM
- AI Agent
- Obsidian / 第二大脑
- 自动化工作流
- 自媒体工具与变现方法

具体规则见：
- `wiki/SCHEMA.md`
- `wiki/index.md`
- `wiki/log.md`

## 如何继续往里加内容

推荐流程：

1. 把新资料放进 `00 Inbox/` 或直接提供 URL
2. 由 AI 执行 ingest：
   - 保存到 `wiki/raw/...`
   - 判断该更新哪些已有页面
   - 必要时创建新页面
   - 更新 `wiki/index.md`
   - 追加 `wiki/log.md`
3. 完成后提交并 push

适合 ingest 的内容：
- YouTube 视频描述 / 字幕
- 网页文章
- 教程笔记
- 会议记录
- 研究资料
- 自己的长笔记或读书笔记

## 推荐使用方式

### 在 Obsidian 中使用
- 直接把这个仓库当作 vault 打开
- 用 `wiki/index.md` 作为入口
- 用图谱视图看页面关系
- 用双链 `[[page-name]]` 在知识之间跳转

### 在 Git 中使用
常用命令：

```bash
git status
git add .
git commit -m "docs: update wiki"
git push
```

### 与 AI Agent 配合
适合让 AI 做的事情：
- 把 Inbox 笔记整理进 Wiki
- 从原始资料抽取实体 / 概念 / 对比页
- 给现有页面补充交叉引用
- 发现重复页面、断链、缺失索引
- 批量维护 YAML frontmatter

## 当前已沉淀的代表性页面

Entities:
- `wiki/entities/obsidian.md`
- `wiki/entities/hermes-agent.md`
- `wiki/entities/claude-code.md`
- `wiki/entities/claude-obsidian.md`

Concepts:
- `wiki/concepts/llm-wiki.md`
- `wiki/concepts/source-ingestion-workflow.md`
- `wiki/concepts/obsidian-ai-workflows.md`
- `wiki/concepts/obsidian-sync-via-git.md`
- `wiki/concepts/slash-command-thinking.md`
- `wiki/concepts/rag-vs-llm-wiki.md`

Comparisons:
- `wiki/comparisons/claude-code-vs-hermes.md`

## 约束与约定

- `wiki/raw/` 里的文件视为原始资料，不直接编辑
- 结构化知识写入 `entities/`、`concepts/`、`comparisons/`、`queries/`
- 新页面必须进入 `wiki/index.md`
- 每次变更应记录到 `wiki/log.md`
- 标签、frontmatter 和页面规范以 `wiki/SCHEMA.md` 为准

## 下一步建议

你可以继续让我做这些事：
- 批量 ingest `00 Inbox/` 中的新资料
- 对整个 wiki 做 lint / 健康检查
- 把某个主题扩展成一个完整专题（例如 Obsidian、Hermes、第二大脑、AI 工作流）
- 为仓库补充自动化脚本，例如批量校验、批量 ingest、索引修复
