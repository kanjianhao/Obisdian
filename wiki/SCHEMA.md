# Wiki Schema

## Domain
这个知识库用于沉淀 AI/LLM、AI Agent、Obsidian/第二大脑、自动化工作流、自媒体工具与变现方法相关的长期知识。

目标不是把资料简单堆进文件夹，而是让 AI 持续维护一个可增长、可交叉引用、可追溯来源的 Markdown Wiki。

## Conventions
- File names: lowercase, hyphens, no spaces. 中文主题优先使用简短拼音/英文 slug，例如 `llm-wiki.md`。
- Every wiki page starts with YAML frontmatter.
- Use `[[wikilinks]]` to link between pages. 每个概念/实体页尽量至少有 2 个出站链接。
- When updating a page, always bump the `updated` date.
- Every new page must be added to `index.md` under the correct section.
- Every action must be appended to `log.md`.
- Raw sources in `raw/` are immutable. 不直接改原始资料；更正和综合写入 `concepts/`、`entities/`、`comparisons/` 或 `queries/`。
- Claims synthesized from 3+ sources should include provenance markers like `^[raw/articles/source-file.md]`.
- 中文内容优先；技术名词可以保留英文。

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
confidence: high | medium | low
contested: false
contradictions: []
---
```

## Raw Source Frontmatter
```yaml
---
source_url: https://example.com/article
ingested: YYYY-MM-DD
sha256: <hex digest of body after frontmatter>
---
```

## Tag Taxonomy
所有页面 tag 必须来自这里。需要新 tag 时，先更新本节，再在页面使用。

### AI / LLM
- ai
- llm
- agent
- prompt-engineering
- rag
- knowledge-base
- model
- benchmark
- inference
- fine-tuning

### Knowledge Management / Obsidian
- obsidian
- wiki
- note-taking
- workflow
- automation
- markdown
- dataview
- git

### Content / Business
- content-creation
- social-media
- monetization
- video
- writing
- tool

### Meta
- comparison
- tutorial
- source
- controversy
- open-question

## Page Thresholds
- Create a page when an entity/concept appears in 2+ sources OR is central to one source.
- Add to an existing page when a source mentions something already covered.
- Do not create pages for passing mentions, minor details, or things outside the domain.
- Split a page when it exceeds ~200 lines.
- Archive a page when its content is fully superseded: move to `_archive/`, remove from `index.md`, and update links.

## Entity Pages
One page per notable person, organization, tool, product, model, plugin, or platform. Include:
- Overview / what it is
- Key facts and dates
- Relationships to other entities via [[wikilinks]]
- Source references

## Concept Pages
One page per concept or topic. Include:
- Definition / explanation
- Current state of knowledge
- Practical workflow or implications
- Open questions or debates
- Related concepts via [[wikilinks]]

## Comparison Pages
Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison, preferably as a table
- Verdict or synthesis
- Sources

## Update Policy
When new information conflicts with existing content:
1. Check dates; newer sources may supersede older sources.
2. If genuinely contradictory, preserve both claims with dates and source links.
3. Mark the contradiction in frontmatter with `contested: true` and `contradictions:`.
4. Flag it in `log.md` for human review.
