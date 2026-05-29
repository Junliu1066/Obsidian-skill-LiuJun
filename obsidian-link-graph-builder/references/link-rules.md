# Link Rules

## Add outbound links when

| Should link | Example |
|---|---|
| Existing method node | `[[数据飞轮]]`, `[[高价值楔子问题]]` |
| Existing case node | `[[Scale AI 从0到1]]`, `[[BOSS直聘从0到1]]` |
| Existing project node | `[[GEO 项目]]`, `[[Agent 知识治理]]` |
| Reusable SOP / Skill node | `[[产品案例拆解 SOP]]`, `[[学习笔记整理 Skill]]` |
| A concept is central to the note | `[[可靠 AI]]`, `[[双边平台冷启动]]` |

## Avoid links when

- The term is generic: 产品、用户、增长、AI.
- The term appears once and has no reuse value.
- No corresponding note exists and it is not worth creating.
- Linking would interrupt reading flow.

## Backlink / index update rules

When linking a new note from an index, use one-line relationship context:

```markdown
- [[Scale AI 从0到1]]：AI 数据基础设施案例，适合学习高价值楔子、数据飞轮、模型评测和可靠 AI 上移路径。
```

Do not add bare links to indexes unless the surrounding style already uses bare links.
