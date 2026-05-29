# Inbox Rules

## Default source patterns

- Desktop product case inbox: `/Users/liujun/Desktop/产品案例收件箱` when available.
- Vault inbox folders named `收件箱`, `inbox`, or `Inbox`.
- User-selected file paths or current note context.

## Type detection

| Signals | Type |
|---|---|
| company/product name, 0-1, cold start, growth, competitor | product case |
| paper title, abstract, method, experiment, arXiv | paper |
| PRD, architecture, API, requirements, project | project document |
| SOP, checklist, framework, method | method/SOP |
| interview, 30秒, 90秒, expression | expression material |
| article, course, notes | learning note |

## Destination suggestions

| Type | Destination pattern |
|---|---|
| product case | `产品经理经验/<case-name>/` or `案例库/<case-name>.md` |
| paper | `AI论文精读/精读卡片库/` |
| method/SOP | `产品方法论/` or `方法论库/` |
| project | `项目/` or existing project folder |
| expression | `面试弹药库/` or `表达卡/` |

Adapt to the user's vault structure. Do not create a new top-level taxonomy if a clear existing one exists.
