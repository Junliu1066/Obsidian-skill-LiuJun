---
name: obsidian-link-graph-builder
description: Build and maintain Obsidian wikilinks, backlinks, index links, and knowledge-graph relationships for Markdown notes. Use when the user asks to 自动出链、链入、补双链、挂索引、整理知识图谱、修复坏链、把新笔记接入知识库.
---

# Obsidian Link Graph Builder

Use this skill to connect an isolated Obsidian note into a knowledge graph by adding meaningful outbound links and updating relevant index / MOC / methodology notes to create backlinks.

## Core principle

Do **not** mechanically link every keyword. Link only stable, reusable knowledge nodes that help future reading, review, migration, or Agent retrieval.

```text
meaningful link = real knowledge relation + existing or worth-creating node + explainable reason
```

## Workflow

1. Read the target note and identify its type: topic, case, method, project, paper, skill, expression card, person, concept, or inbox material.
2. Extract candidate entities:
   - product / company / project names
   - methods, SOPs, frameworks, metrics
   - related projects or interview assets
   - people, papers, concepts if important
3. Scan the vault for candidate notes using filenames, titles, aliases, tags, headings, and existing index notes.
4. Classify candidates:
   - **strong link**: add wikilink directly;
   - **weak link**: report as suggestion;
   - **no real relation**: skip.
5. Add outbound links to the target note with natural wording.
6. Update relevant index / MOC / methodology notes to link back to the target note.
7. Add relationship explanations when updating index notes.
8. Check for broken links, duplicate links, over-linking, and wrong path formats.
9. Output a link handling report.

## Read references when needed

- For link rules and examples, read `references/link-rules.md`.
- For node taxonomy, read `references/node-taxonomy.md`.
- For report templates, read `references/templates.md`.

## Safety rules

- Preserve existing frontmatter, headings, Dataview blocks, and user wording unless editing is necessary.
- Do not create many empty notes unless the user asks.
- Prefer existing note names and aliases.
- Use Obsidian wikilinks: `[[note-name]]` or `[[folder/note-name|alias]]`.
- For vault file references in chat, use clickable wikilinks.
- If unsure whether a link is meaningful, report it as a suggestion instead of editing.

## Output format

```markdown
## 链接处理报告

### 已添加出链
| 当前笔记位置 | 链接到 | 关系说明 |
|---|---|---|

### 已补充链入
| 被更新的索引 / 方法论笔记 | 新增链接 | 关系说明 |
|---|---|---|

### 建议新建但未创建的节点
- `[[...]]`：原因

### 跳过的弱相关链接
- `...`：原因

### 检查结果
- 坏链：...
- 重复链接：...
- 过度链接风险：...
```
