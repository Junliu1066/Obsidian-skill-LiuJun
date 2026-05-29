# Obsidian + Codex Skill 包清单

> 更新时间：2026-05-29

## 这是什么？

这是一个给 **Obsidian + Codex** 使用的轻量 Skill 包，核心目标是帮助你把零散资料变成可复用的学习资产。

它不是一个“插件合集”，也不是一堆复杂自动化脚本，而是两套最常用、最稳定的 AI 工作流：

1. **整理学习笔记**：把杂乱的文章、访谈、课程笔记、Markdown 文档整理成结构清晰的学习版笔记。
2. **拆解产品案例**：把一个产品、公司或商业案例，拆成机会判断、竞品差异、真实痛点、MVP、增长飞轮、风险和表达素材。

一句话理解：

> 这个包的作用，是让 Codex 按固定 SOP 帮你整理 Obsidian 笔记和拆解产品案例，而不是每次都从零提示。

---

## 适合谁用？

这个 Skill 包适合：

- 想用 Obsidian 搭建个人知识库的人；
- 想系统学习产品思维、商业案例、AI 产品的人；
- 想把文章、案例、课程、访谈整理成长期可复用笔记的人；
- 想训练面试表达、产品分析能力、案例拆解能力的人；
- 想让 Codex / Agent 按自己的方法论稳定工作的用户。

不适合：

- 只想简单记流水账的人；
- 不使用 Codex / AI Agent 的人；
- 期待一键自动搭完整知识库、完全不用自己判断的人。

---

## 这个包解决什么问题？

很多人用 Obsidian 会遇到三个问题：

| 问题 | 表现 | 这个包怎么解决 |
|---|---|---|
| 笔记太乱 | 摘抄很多，但没有结构，之后很难复习 | 用 `learning-note-refiner` 自动整理成摘要、速览、图谱、流程图和 SOP |
| 案例太浅 | 只知道一个产品成功了，但讲不清为什么 | 用 `product-case-methodology` 拆机会、竞品、痛点、MVP、增长、飞轮和风险 |
| 经验不能复用 | 每次分析都重新想框架，输出不稳定 | 把常用分析流程固化成 Skill，让 Codex 每次按同一套 SOP 工作 |

核心不是“让 AI 帮你写更多文字”，而是：

```text
原始资料
→ 清洗整理
→ 结构化笔记
→ 方法论沉淀
→ 产品案例拆解
→ 面试 / 项目 / 表达复用
```

---

## 包含的 Skill

| Skill | 作用 | 使用场景 |
|---|---|---|
| `learning-note-refiner` | 整理 Obsidian / Markdown 笔记：去重、摘要、知识图谱、流程图、SOP、缺失信息补充 | 当你有一篇原始笔记、文章、访谈稿、学习资料，需要整理成结构清晰的学习版笔记 |
| `product-case-methodology` | 产品案例拆解：0-1、竞品差异、真实痛点、MVP、冷启动、增长、飞轮、风险、面试表达 | 当你要拆解一个产品 / 公司 / 商业案例，比如 Scale AI、Airbnb、BOSS 直聘、抖音等 |
| `obsidian-link-graph-builder` | 自动出链 / 链入：补充有意义双链，更新索引、方法论和项目节点 | 当你写完一篇新笔记，需要把它接入 Obsidian 知识图谱 |
| `inbox-to-knowledge-graph` | 收件箱自动入库：识别资料类型、清洗结构化、生成节点、更新索引 | 当你把资料丢进收件箱，需要自动分类入库 |

---

## 四个 Skill 分别怎么用？

### 1. learning-note-refiner：整理学习笔记

适合处理：

- 原始文章；
- 课程笔记；
- 访谈稿；
- 长 Markdown 文档；
- Obsidian 里写得比较散的学习笔记。

你可以这样对 Codex 说：

```text
整理这篇笔记，去重，加顶部摘要、一页速览、知识图谱、流程图和后续补充建议。
```

```text
把当前 Obsidian 笔记处理成学习版，保留核心观点，补 SOP 和检查清单。
```

它通常会输出 / 补充：

```text
顶部摘要
→ 一页速览
→ 知识图谱
→ 全流程图
→ 模块化拆解
→ SOP / Checklist
→ 缺失信息与后续补充建议
```

---

### 2. product-case-methodology：拆解产品案例

适合处理：

- 产品从 0 到 1；
- 冷启动案例；
- 增长案例；
- 商业模式案例；
- AI 产品案例；
- 面试中的产品案例题。

你可以这样对 Codex 说：

```text
拆解 Scale AI 从 0 到 1，按产品经理案例分析方式整理。
```

```text
分析这个产品为什么能成功，它和竞品的差异是什么，真实痛点是什么。
```

```text
把这个案例整理成：机会判断、MVP、竞品破局、真实早期痛点、增长飞轮、风险和面试表达。
```

它会重点回答：

```text
它做了什么
→ 为什么成功
→ 对比竞品抓住了什么差异
→ 早期真实痛点是什么
→ MVP 怎么验证
→ 0-1 后怎么发展
→ 遇到什么问题
→ 怎么解决
→ 有什么飞轮、壁垒和风险
→ 怎么迁移到面试表达
```

---

### 3. obsidian-link-graph-builder：自动出链 / 链入

适合在新笔记整理完成后使用，把它接入知识图谱。

```text
请用 obsidian-link-graph-builder 处理当前笔记：补充有意义的出链，把它链入相关索引、方法论和项目节点，不要机械链接普通词，最后输出链接处理报告。
```

---

### 4. inbox-to-knowledge-graph：收件箱自动入库

适合在你把新资料丢进收件箱后使用。

```text
请用 inbox-to-knowledge-graph 处理收件箱最新文件：保留原始资料，判断类型，生成结构化笔记，更新相关索引，并输出入库报告。
```

---

## 推荐使用顺序

最推荐的用法是：

```text
原始资料 / 笔记
→ inbox-to-knowledge-graph 判断类型并入库
→ learning-note-refiner 整理成学习笔记
→ product-case-methodology 拆成产品案例、方法论、面试表达
→ obsidian-link-graph-builder 补出链 / 链入 / 索引
```

如果你只是整理文章，用第一个 Skill 就够了。

如果你是在拆产品、公司、商业案例，用第二个 Skill。

如果你先收集了一堆资料，再想做深度案例分析，就先用 `learning-note-refiner` 清洗，再用 `product-case-methodology` 拆解。

---

## 推荐 Obsidian 目录结构

你可以在 Obsidian 里先建 4 类入口：

```text
学习索引/
案例库/
方法论库/
表达卡/
```

一个简单结构可以是：

```text
Obsidian Vault/
├── 学习索引.md
├── 案例库/
│   ├── Scale AI 从0到1.md
│   ├── Airbnb 从0到1.md
│   └── BOSS直聘从0到1.md
├── 方法论库/
│   ├── 高价值楔子问题.md
│   ├── 双边平台冷启动SOP.md
│   └── 数据飞轮.md
└── 表达卡/
    ├── 产品案例面试表达卡.md
    └── 项目迁移表达卡.md
```

---

## 安装方式

把 `skills/` 下面的四个文件夹复制到你的 Codex skills 目录：

```text
~/.codex/skills/
```

最终应该长这样：

```text
~/.codex/skills/
├── learning-note-refiner/
├── product-case-methodology/
├── obsidian-link-graph-builder/
└── inbox-to-knowledge-graph/
```

复制完成后，重启 Codex / 重新打开会话，让 Skill 被重新加载。

---

## 文件夹结构

```text
Obsidian-Codex-Skill包/
├── 00-Skill包清单.md
├── 01-使用说明.md
└── skills/
    ├── learning-note-refiner/
    │   ├── SKILL.md
    │   ├── agents/
    │   └── references/
    ├── product-case-methodology/
    │   ├── SKILL.md
    │   ├── agents/
    │   └── references/
    ├── obsidian-link-graph-builder/
    │   ├── SKILL.md
    │   └── references/
    └── inbox-to-knowledge-graph/
        ├── SKILL.md
        └── references/
```


---

## 配套说明文档

除了四个 Skill，本包还附带几份说明文档，方便你发给别人理解和使用：

| 文档 | 作用 |
|---|---|
| `README.md` | GitHub 仓库首页介绍，说明这个 Skill 包是什么、怎么安装、怎么使用 |
| `01-使用说明.md` | 更简洁的安装和触发方式说明 |
| `02-为什么要做Skill包.md` | 解释为什么在 Obsidian 场景下要把高频流程做成 Skill |
| `03-发给Codex的第二大脑功能增强Prompt.md` | 可直接复制给 Codex，让它帮你把 Vault / 仓库升级成显性第二大脑 |

其中 `03-发给Codex的第二大脑功能增强Prompt.md` 是给使用者看的可复制 Prompt。它会引导 Codex 帮你补充：

- 第二大脑理念说明文档；
- Mermaid 架构图；
- 第二大脑知识节点模板；
- Agent 读取知识库的规则；
- 对外表达版本。

---

## 不包含的 Skill

本包已包含自动出链 / 链入和收件箱自动入库；暂不包含以下能力：

- 论文阅读 Skill；
- Bad Case 复盘 Skill；
- 文章人味化 Skill；
- 事实准确性审查 Skill。

如果后续需要，可以再单独扩展。

---

## 最后一句话

> 这个包的价值，不是替你“多写几篇笔记”，而是帮你把 Obsidian 里的学习、案例和方法论整理成可复用的知识资产，让 Codex 按稳定 SOP 持续协助你学习、拆解和表达。
