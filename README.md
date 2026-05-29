# Obsidian + Codex Skill Pack

一个轻量的 Codex Skill 包，用于配合 Obsidian 搭建个人学习系统、整理 Markdown 笔记、拆解产品案例，并沉淀可复用的方法论和表达素材。

## 这个仓库是什么？

这个仓库包含四个 Codex Skill：

| Skill | 作用 |
|---|---|
| `learning-note-refiner` | 将 Obsidian / Markdown 学习笔记整理成结构化学习文档，包括去重、摘要、一页速览、知识图谱、流程图、SOP 和缺失信息补充。 |
| `product-case-methodology` | 拆解产品 / 公司 / 商业案例，包括 0-1、竞品差异、真实痛点、MVP、冷启动、增长飞轮、风险、壁垒和面试表达。 |
| `obsidian-link-graph-builder` | 自动出链 / 链入：给当前笔记补有意义的双链，并把新笔记挂到相关索引、方法论和项目节点。 |
| `inbox-to-knowledge-graph` | 自动入库：处理收件箱资料，识别类型、清洗结构化、生成知识节点并更新索引。 |

它的目标不是替你堆更多笔记，而是让 Codex 按稳定 SOP 帮你把资料转化为可复用的知识资产。

```text
原始资料 / 笔记
→ learning-note-refiner 清洗整理
→ product-case-methodology 深度拆解
→ obsidian-link-graph-builder 补双链 / 挂索引
→ inbox-to-knowledge-graph 处理后续收件箱资料
→ Obsidian 中沉淀为案例、方法论和表达卡
```

## 适合谁？

适合以下用户：

- 使用 Obsidian 管理学习资料和知识库的人；
- 想系统学习产品思维、AI 产品、商业案例的人；
- 想把文章、访谈、课程笔记整理成长期可复用笔记的人；
- 想训练产品案例拆解、面试表达、方法论沉淀能力的人；
- 想让 Codex / AI Agent 按固定工作流稳定处理重复学习任务的人。

## 仓库结构

```text
Obsidian-Codex-Skill包/
├── README.md
├── 00-Skill包清单.md
├── 01-使用说明.md
├── 02-为什么要做Skill包.md
├── 03-发给Codex的第二大脑功能增强Prompt.md
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

## 安装方式

将 `skills/` 目录下的四个 Skill 文件夹复制到你的 Codex skills 目录：

```bash
cp -R skills/learning-note-refiner ~/.codex/skills/
cp -R skills/product-case-methodology ~/.codex/skills/
cp -R skills/obsidian-link-graph-builder ~/.codex/skills/
cp -R skills/inbox-to-knowledge-graph ~/.codex/skills/
```

安装后目录应类似：

```text
~/.codex/skills/
├── learning-note-refiner/
├── product-case-methodology/
├── obsidian-link-graph-builder/
└── inbox-to-knowledge-graph/
```

然后重启 Codex 或重新打开会话，让 Skill 被重新加载。

## 使用示例

### 1. 整理学习笔记

适合处理原始文章、课程笔记、访谈稿、长 Markdown 文档、Obsidian 笔记。

你可以对 Codex 说：

```text
整理这篇笔记，去重，加顶部摘要、一页速览、知识图谱、流程图和后续补充建议。
```

或：

```text
把当前 Obsidian 笔记处理成学习版，保留核心观点，补 SOP 和检查清单。
```

典型输出结构：

```text
顶部摘要
→ 一页速览
→ 知识图谱
→ 全流程图
→ 模块化拆解
→ SOP / Checklist
→ 缺失信息与后续补充建议
```

### 2. 拆解产品案例

适合处理产品从 0 到 1、冷启动、增长、商业模式、AI 产品、平台型产品等案例。

你可以对 Codex 说：

```text
拆解 Scale AI 从 0 到 1，按产品经理案例分析方式整理。
```

或：

```text
分析这个产品为什么能成功，它和竞品的差异是什么，真实痛点是什么。
```

典型拆解链路：

```text
它做了什么
→ 为什么成功
→ 对比竞品抓住了什么差异
→ 早期真实痛点是什么
→ MVP 怎么验证
→ 0-1 后怎么发展
→ 遇到什么问题
→ 怎么解决
→ 飞轮、壁垒和风险
→ 面试表达 / 项目迁移
```


### 3. 自动出链 / 链入

适合当你写完一篇笔记，需要把它接入 Obsidian 知识图谱。

```text
请用 obsidian-link-graph-builder 处理当前笔记：补充有意义的出链，把它链入相关索引、方法论和项目节点，不要机械链接普通词，最后输出链接处理报告。
```

### 4. 收件箱资料自动入库

适合当你把文章、产品案例、论文或项目资料丢进收件箱后，需要自动清洗、分类、入库。

```text
请用 inbox-to-knowledge-graph 处理产品案例收件箱最新文件：保留原始资料，判断类型，生成结构化笔记，更新相关索引，并输出入库报告。
```

## 推荐 Obsidian 使用方式

建议在 Obsidian 中至少建立四类入口：

```text
学习索引/
案例库/
方法论库/
表达卡/
```

示例结构：

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

推荐工作流：

```text
资料进入 Obsidian
→ 用 learning-note-refiner 清洗整理
→ 用 product-case-methodology 做产品拆解
→ 把方法论和表达卡沉淀到索引里
```


## 第二大脑功能增强 Prompt

仓库里提供了一个可直接复制给 Codex 的 Prompt：

```text
03-发给Codex的第二大脑功能增强Prompt.md
```

它的作用是让 Codex 帮你把 Obsidian Vault / Skill 包进一步升级成“显性第二大脑”：

```text
显性记忆
→ 本地文件
→ Obsidian 知识图谱
→ Skill 固化流程
→ 任意 AI 可接入
→ 用户保持控制权
```

### 怎么用？

1. 在 Codex 中打开你的 Obsidian Vault 或这个 Skill 包仓库。
2. 打开 `03-发给Codex的第二大脑功能增强Prompt.md`。
3. 复制其中“可直接复制给 Codex 的 Prompt”。
4. 发给 Codex。
5. 如果你想先看计划，就在 Prompt 前加：`先不要改文件，先给我计划和文件清单。`
6. 如果你想直接执行，就说：`请直接新增文档和模板，完成后报告改了哪些文件。`
7. 完成后检查 Codex 新增的第二大脑说明、节点模板、Agent 读取规则和架构图。

这个增强 Prompt 的核心思想是：不要只依赖某个 AI 的隐式 memory，而是把你的知识、项目、案例、方法论和偏好沉淀成一个你自己拥有的、显性的、可迁移的个人 Wiki。Obsidian 负责保存和连接知识，Skill 负责固化流程，Codex / Claude / 其他 AI 只是可替换的执行器。

## 不包含什么？

这个包保持轻量，包含学习笔记整理、产品案例拆解、自动双链和收件箱入库四个核心 Skill。

暂不包含：

- 论文阅读 Skill；
- Bad Case 复盘 Skill；
- 文章人味化 Skill；
- 事实准确性审查 Skill。

后续可以按需要单独扩展。

## 设计理念

这个 Skill Pack 的核心思想是：

> Obsidian 负责沉淀知识结构，Codex 负责按 Skill 执行高复用流程。两者结合，可以把零散资料持续转化成可复习、可迁移、可表达的知识资产。

不是让 AI 代替你思考，而是让 AI 帮你稳定执行已经沉淀好的学习 SOP。

## License

可根据你的使用场景自行补充 License。
