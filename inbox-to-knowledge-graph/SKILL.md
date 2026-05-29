---
name: inbox-to-knowledge-graph
description: Process Obsidian inbox materials into structured knowledge-graph notes. Use when the user asks to 处理收件箱、导入资料、清洗入库、自动入库、把新资料挂到知识图谱、从产品案例收件箱处理最新文件.
---

# Inbox to Knowledge Graph

Use this skill to process raw inbox files into structured Obsidian knowledge nodes, preserving originals and updating relevant indexes.

## Core principle

Inbox processing is not just moving files. It is a pipeline:

```text
raw material → backup/original preservation → type detection → cleaning → structured note → links/indexes → reusable method or skill suggestion
```

## Workflow

1. Locate the inbox file or latest inbox item.
2. Preserve the original:
   - do not overwrite source material;
   - create an original import copy or keep source path metadata.
3. Detect material type:
   - product/company case;
   - article/learning note;
   - paper;
   - project document;
   - method/SOP;
   - interview/expression material;
   - unknown.
4. Choose processing path:
   - product case → use product-case style structure;
   - learning note/article → use learning-note style structure;
   - paper/project/method → create a structured node and migration section.
5. Clean and structure the note:
   - frontmatter;
   - summary;
   - one-page overview;
   - key facts / opinions / inferences / unknowns;
   - knowledge graph or flowchart when useful;
   - reusable SOP or project migration.
6. Place the note in the appropriate folder.
7. Update relevant indexes/MOCs.
8. Add meaningful wikilinks or call `obsidian-link-graph-builder` if available.
9. Output an import report.

## Read references when needed

- `references/inbox-rules.md`: file detection and destination rules.
- `references/templates.md`: import card and report templates.
- `references/index-update-rules.md`: how to update indexes safely.

## Safety rules

- Never delete the inbox source file unless the user explicitly asks.
- Never overwrite an existing processed note without backup.
- If destination is ambiguous, create a clearly named draft or ask the user.
- Keep source path and processing date in frontmatter when possible.
- Use relative vault paths in notes; use wikilinks in responses.

## Output format

```markdown
## 入库处理报告

### 已处理文件
- 来源：...
- 类型：...
- 目标笔记：[[...]]

### 已生成内容
- 摘要：...
- 图谱/流程图：...
- 方法论/SOP：...
- 项目迁移：...

### 已更新索引
| 索引笔记 | 新增内容 |
|---|---|

### 后续建议
- ...
```
