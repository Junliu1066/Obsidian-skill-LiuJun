---
name: learning-note-refiner
description: Refine Obsidian or Markdown learning notes into concise, readable, study-friendly documents. Use when the user asks to process an entire note/article, remove duplicate semantic content, add a top summary, restructure headings, add learning aids such as Mermaid mind maps, tree diagrams, flowcharts, tables, checklists, SOPs, missing-knowledge sections, or preserve/repair Obsidian wikilinks. Also use by default when the user says “整理”, “整理全文”, “处理整篇”, “去重”, “加摘要和图表”, “做成学习版”, “优化阅读体验”, or similar shorthand.
---

# Learning Note Refiner

Use this skill to turn long, repetitive learning notes into a clean study version while preserving the user’s knowledge assets.

## Default trigger convention

When the user says “整理” with a current note or selected article context, automatically treat it as:

> Use this skill to refine the whole current note/article: create a backup, remove semantic duplication, add a top summary, add suitable Mermaid diagrams/tables, improve reading structure, and list missing knowledge.

## Default workflow

1. **Confirm scope from context**: use the current note or selected note path. If editing destructively, create a backup copy first unless the user explicitly says not to.
2. **Read the full note**: inspect frontmatter, headings, existing links, repeated sections, diagrams, and embedded assets.
3. **Build a content map**: identify the main learning modules, repeated meanings, method/SOP blocks, examples, and interview/project transfer sections.
4. **Deduplicate semantically**: merge repeated explanations; keep the strongest version; preserve unique facts, metrics, templates, and links.
5. **Add top learning layer**: add a concise top summary, one-page table, reading guide, and knowledge graph.
6. **Add visual aids**: use Mermaid diagrams where useful: mindmap for concept map, flowchart for process, tree for hierarchy, loop for flywheel.
7. **Restructure for reading**: use clear numbered sections, short paragraphs, tables, and “一句话总结”.
8. **Add missing-knowledge section**: list what still needs verification, citations, examples, risks, metrics, or follow-up notes.
9. **Preserve Obsidian compatibility**: keep YAML frontmatter, wikilinks, tags, and Dataview blocks intact unless asked.
10. **Report changes**: mention backup path, major edits, new skill/notes created, and how to use the result.
11. **Optional high-reuse audit**: if the user asks to check correctness, misleading claims, source quality, or high-risk statements after refinement, use `$note-accuracy-auditor` and output a separate chat report; do not insert that report into the note unless explicitly requested.

## Output structure for a refined note

Adapt to the note, but default to this structure:

1. YAML frontmatter.
2. `# Title`.
3. Top callout summary: `> [!summary] 顶部摘要`.
4. `## 一页速览` table.
5. `## 知识图谱` with a Mermaid mind map.
6. `## 全流程图` with a Mermaid flowchart.
7. Numbered main modules. For each module, prefer:
   - 原始事实
   - 拆解与方法论
   - SOP / 检查清单
   - 产品经理视角 / 学习启发
8. `# 缺失信息与后续补充建议`.
9. `# 一句话总复盘`.

## Deduplication rules

- Merge repeated concepts into one canonical section.
- Keep original examples if they illustrate different points.
- Keep metrics, dates, and claims, but mark items that need sources if provenance is unclear.
- Do not delete user-specific links or project-transfer sections unless duplicated.
- Prefer “原始事实 → 方法论 → SOP → 视角 → 指标 → 迁移” over repeated long commentary.

## Diagram selection guide

- **Mind map**: use for full-note concept overview.
- **Flowchart**: use for step-by-step methods, MVP, cold start, growth, resource loops.
- **Tree diagram**: use for hierarchy, user segmentation, supply/demand split, product modules.
- **Flywheel loop**: use for growth/data feedback loops.
- **Table**: use for comparison, SOP steps, metrics, PM perspectives, migration to user projects.

Use Mermaid in Markdown, because Obsidian can render it directly.

## Missing-knowledge checklist

Always scan whether the note lacks:

- Source/citation for important historical claims or metrics.
- Timeline of key events.
- Definitions of key concepts.
- Metrics and decision thresholds.
- Risks, compliance, and edge cases.
- Competitors and alternatives.
- Unit economics or cost-benefit thinking.
- User segmentation and scenario boundaries.
- Interview expression templates.
- Links to related notes and reusable SOPs.

## Safety rules

- Create a backup before major rewrite.
- Avoid absolute paths in Obsidian responses; use wikilinks for vault files.
- Preserve frontmatter fields unless updating `status` or `updated` is appropriate.
- Do not remove unique user insights; condense and relocate them.
- If the note is too long, rewrite in a single clean pass and then verify headings/links.

## When more detail is needed

Load only the relevant reference:

- `references/refinement-templates.md`: complete templates for summaries, diagrams, and reports.
- `references/diagram-patterns.md`: reusable Mermaid diagram patterns.
