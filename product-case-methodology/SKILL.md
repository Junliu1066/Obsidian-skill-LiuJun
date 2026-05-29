---
name: product-case-methodology
description: Analyze product/company cases from either selected text or just a product name. Use for PM case拆解, 0-1, cold start, growth, competitor break-through, opportunity discovery, success/failure attribution, post-0-1 development, growth problems/solutions, data/business flywheels, SOPs, interview-ready cards, and Obsidian note updates. Must answer what it did, why it succeeded, what it captured versus competitors (or how the opportunity was discovered if no clear competitor), how it developed after 0-1, what problems appeared, and how it solved them. Learn from user feedback by updating the skill references/iteration memory when the user says to align or improve the SOP.
---

# Product Case Methodology

Use this skill to transform product-case fragments into structured PM learning assets. The user wants **new knowledge input**, not a context-only summary. Treat the selected text as a starting hypothesis, then expand it with real product/business mechanisms.

## Default trigger convention

When the user has selected editor text and says only “拆解”, “分析一下”, “补充一下”, “沉淀一下”, or similar shorthand, automatically treat it as:

> Use this skill to analyze the selected text, supplement missing product knowledge, and append methodology/SOP/PM perspectives below the selected passage unless the user asks otherwise.

## Primary workflow for only a product/company name

When the user gives only a product/company name or asks for an independent拆解:
1. Verify the object and use current public sources for facts that may have changed (leadership, funding, customers, competitors, regulation, product lines). Cite sources when used.
2. Load `references/independent-case-sop.md` for the full framework.
3. Always answer the six questions: **what it did; why it succeeded; what it captured versus competitors; how it developed after 0-1; what problems appeared; how it solved them**.
4. Branch correctly: if competitors/substitutes exist, do **not** write a “no obvious competitor” branch in the case output; analyze **market demand → product scheme → MVP/landing loop → competitor gap + break-through path**. Only if competitors/substitutes truly cannot be identified, analyze opportunity discovery path instead of inventing competitors.
5. Extract the cognitive difference as **not X, but Y**; reconstruct how the product was thought through and built from market demand to product plan to landing loop, then cover MVP, cold start/GTM, growth levers, data/business flywheel, moat, risks, and interview transfer.
6. If the user asks to入库, create/update the experience pack, full case, interview card, and Obsidian indexes.

## Learning / iteration protocol

The **skill is the source of truth**. When the user corrects the拆解方法 or says “以后要… / 写进 skill / 这个标准记住 / 迭代 skill”: update this skill itself—usually `references/iteration-memory.md` plus the relevant framework/template reference. Do **not** treat an Obsidian SOP note as the primary iteration target. Only sync a vault SOP/note when the user explicitly asks for documentation, or when it is useful as a human-readable mirror of the skill. Keep changes minimal and report which skill files changed.

## Optional high-reuse accuracy audit

After a full product case/article is processed, if the user asks to check correctness, avoid misleading claims, or run a high-reuse verification pass, use `$note-accuracy-auditor`. That audit must output a separate chat report and must not write into the article unless explicitly requested.

## Primary workflow for selected text

When an `editor_selection` is present:
1. Treat the selected text as the target case fragment.
2. Read the surrounding note only if needed to avoid duplicate sections or to preserve structure.
3. Identify the case stage: demand source, opportunity discovery, MVP, 0-1 validation, cold start, growth, retention, monetization, scaling, or organization/resource constraint.
4. Extract facts from the selected text, but do **not** stop there. Separate: **given facts / domain knowledge / inference / unknowns to verify**.
5. Add knowledge expansion: explain the underlying mechanism, industry background, competitor context, user-behavior logic, product/operation/data loops, and comparable cases when useful.
6. Convert the expanded analysis into PM methodology: assumptions, decision logic, SOP steps, metrics, risks, and reusable templates.
7. Always add success/failure attribution when the case has an outcome: explain **why it could succeed or fail**, separating structural timing, user insight, differentiation, execution/resources, feedback loops, and defensibility. If evidence is insufficient, label the attribution as inference and list what must be verified.
8. Add missing PM perspectives from the checklist below.
9. If the user asks to “补充/写到下面/沉淀”, append a concise but complete section below the selected passage or before the next same-level heading. Preserve the user’s original wording.
10. If working in an Obsidian vault, use wikilinks for related notes and do not overwrite unrelated content.

## Standard output structure

Use only the sections that fit the selected text; avoid forcing all sections if the case is small.

```markdown
### 我们能从中学到什么
### 事实、推断与待验证信息
### 它做了什么
### 为什么能成功 / 成败归因
### 竞品/替代方案与破局点
### 如果无明显竞品：机会发现路径
### 认知差在哪里：不是 X，而是 Y
### 为什么不是简单模仿
### 旧模式的成本结构
### 谁是付费方、稀缺侧和弱势侧
### 关键驱动点是什么
### MVP 与最小闭环
### 冷启动 / GTM / 增长杠杆
### 0-1 之后的发展路径
### 发展中遇到的问题与解决方式
### 新机制如何改变旧效率
### 创新扩散如何发生
### 关键机制拓展
### 方法论拆解
### 可沉淀的 SOP
### 产品经理应该具备的视角
### 易遗漏知识点补充
### 指标与判断标准
### 面试表达模板
### 可迁移到我的项目
```

## PM perspective checklist

Always scan for missing perspectives:

- **User / scenario / JTBD**: who is the user, in what situation, completing what task?
- **Pain intensity**: high frequency, high urgency, high willingness to pay, or high emotional intensity?
- **Existing alternatives**: what did users do before this product?
- **MVP / hypothesis validation**: which biggest uncertainty is being tested?
- **Two-sided marketplace**: supply side, demand side, key side, liquidity, trust, matching quality.
- **Atomic network**: the smallest local market where density can form.
- **Supply quality**: supply count, quality, availability, response speed, reliability.
- **Trust / risk**: identity, authenticity, safety, payments, disputes, guarantees, moderation.
- **Incentive alignment**: why each side joins, stays, contributes, and avoids bypassing the platform.
- **Channel / GTM**: where users appear when the pain occurs; how the product reaches them.
- **Metrics**: activation, conversion, retention, liquidity, satisfaction, unit economics.
- **Stage gates**: continue, pivot, scale, or stop signals.
- **Truth grounding**: distinguish selected-text facts, outside/domain facts, inference, and unknowns; avoid turning notes into unsupported conclusions.
- **Mechanism expansion**: explain why the behavior or result happens, not just what happened; include competitor context, user psychology, transaction/content loops, algorithms, operations, and constraints.
- **Success/failure attribution**: why this case could succeed or fail; check timing, underserved user, differentiated insight, MVP proof, execution density, resource advantage, data/algorithm/operation loops, network effects, and defensibility.
- **What it did concretely**: avoid category labels; identify product form, key workflow, user/customer, business model, and minimum successful action.
- **Competitor break-through vs opportunity discovery**: if competitors/substitutes exist, compare gaps and break-through and do not include a no-competitor branch; if not, trace opportunity origin, why others missed it, and why now.
- **Post-0-1 development**: cover 1-10/10-100 evolution, platformization, monetization, ecosystem expansion, or strategic shifts.
- **Growth problems and solutions**: name the stage-specific problems and the product/operation/governance/strategy actions used to solve them.
- **Named competitor differentiation**: when several adjacent competitors matter, add a named competitor matrix comparing JTBD, value-chain control point, product form, supply/quality mechanism, workflow depth, moat, risks, and a memorable PM label.
- **Real early-platform pain**: for platform/infrastructure/B2B workflow cases, explain what was actually hard in 0-1—task definition, workflow splitting, supply organization, quality control, cost/efficiency, outcome proof, customer trust, and repeatable productization.
- **Manual-to-productized**: which early manual operations become process, rules, product features, or dashboards.
- **Interview transfer**: how to express the insight as PM thinking without pretending it is personal work experience.
- **Cognitive difference vs imitation**: what old assumption the product rejects, what new judgment it validates, and why simply copying surface features would not work.
- **Old-model cost structure**: who pays, who bears wasted time/money/risk, who is underserved, and what mechanism keeps the inefficiency recurring.
- **Problem size / pain intensity / driver point**: whether the issue affects core business results, who is most painful, and which bottleneck unlocks the whole chain.
- **Paid side vs scarce side vs weak side**: in platforms, do not equate the paying side with the priority side; identify who decides experience quality and long-term trust.
- **Distribution mechanism**: search, recommendation, feeds, direct communication, or agent routing; explain how the mechanism reallocates attention/opportunity and what new data flywheel it creates.
- **Short-term revenue vs long-term ecosystem**: identify governance or monetization choices that sacrifice immediate extraction to protect trust, retention, or supply quality.
- **Innovation diffusion**: identify innovators/early adopters, edge-market entry, perceived benefit, repeatable proof, productized operations, and mainstream adoption barriers.

## Methodology patterns

### Demand analysis
Use this chain:

**abnormal/strong scenario → target user → urgent pain → existing solution gap → MVP → core hypothesis → scalable opportunity.**

### 0-1 validation
Use this chain:

**specific scenario → MVP → small-sample feedback → diagnose demand/channel/supply/product issues → find high-density scenario → identify strong-love users → redefine product → find growth lever → reusable loop.**

### Full independent product case
Use this chain for full cases:

**what it did → why it succeeded → competitor/substitute gap or opportunity discovery → not X but Y → MVP/minimum loop → cold start/GTM → post-0-1 development → stage problems → solutions → flywheel/moat/risk → interview transfer.**

If this is the user's only product name request, load `references/independent-case-sop.md`.

### Success/failure attribution
Use this chain whenever a case has an outcome:

**structural timing → underserved user/scenario → non-consensus insight → differentiated product/operation choice → MVP or data proof → execution/resource leverage → feedback loop/network effect → defensibility → measurable result.**

Separate facts from inference. Do not say “it succeeded because it executed well” only; name the concrete mechanism that turned the choice into results.

### Truth-grounded expansion
Use this chain before writing conclusions:

**selected-text claim → what is factually known → what external/domain knowledge explains it → what mechanism caused the result → what is inference → what needs verification.**

Avoid shallow phrases such as “踩中红利”“形成闭环”“运营能力强” unless the concrete mechanism is named. Prefer explanations like: **uncovered scenario → lower decision cost → recommendation feedback loop → creator/content supply expansion → retention improvement**.

### Two-sided marketplace cold start
Use this upgraded chain:

**define minimum transaction → choose atomic network → split supply/demand → identify key side → manually seed key side → build trust and quality bar → create first positive feedback → bring the other side → monitor liquidity metrics → diagnose transaction blockers → calculate unit economics → productize manual work → replicate to next market.**

### Growth lever analysis
Use this chain:

**growth goal → current funnel → biggest blocker → user/job reason → high-leverage action → metric change → productized mechanism → risks and constraints.**

### Cognitive-difference analysis
Use this when a case compares with competitors or mentions 0-1 innovation:

**competitor surface feature → competitor/default assumption → structural inefficiency caused by the old assumption → new non-consensus judgment → product mechanism that tests it → data/feedback proving or disproving it → defensibility if incumbents copy the feature.**

Also separate **copyable features** from **hard-to-copy mechanisms** such as user mindshare, supply quality, distribution rules, trust governance, proprietary data, operations, and ecosystem incentives.

### Imitation-failure analysis
Use this when the user asks why a copycat product failed or why copying is risky:

**surface imitation → no migration reason → no new supply/distribution/trust/cost advantage → incumbent has mindshare/data/network effects → higher cold-start cost → low retention or weak conversion exposes pseudo-demand.**

Avoid absolute claims like “all imitation fails.” Prefer: **imitation without cognitive difference and mechanism difference usually fails.**

### Problem-value and driver-point analysis
Use this when the selected text mentions problem size, pain, value, or “驱动点”:

**surface request → underlying workflow problem → affected business metric → actor bearing the highest cost → key bottleneck / driver point → MVP to verify improvement → metric proving business value.**

Shortcut formula: **business value = problem scale × pain intensity × driver-point position × verifiable loop.**

### Platform key-side and governance analysis
Use this for marketplaces, communities, recruitment, content, GEO platforms, or Agent ecosystems:

**paid side → scarce side → weak/risk-bearing side → side that determines experience floor → side that generates critical data → governance choice → monetization tradeoff → long-term ecosystem effect.**

Do not assume the paid side should always be prioritized. Explain when protecting a scarce or weak side creates more value for the paid side over time.

### Mechanism-shift analysis
Use this when a product changes search to recommendation, offline to online, manual to agentic, content quantity to quality, or one-way flow to interaction:

**old mechanism → where friction/concentration/waste occurs → new mechanism → what cost it lowers → what behavior data it captures → how the data improves the mechanism → what risks/gaming/fairness issues appear.**

### Innovation-diffusion analysis
Use this when a case mentions edge entry, early adopters, cold start, or scaling from 0-1:

**structural problem → most painful early adopters → cognitive MVP → minimum transaction/usage loop → perceived benefit → repeatable proof/case → manual actions productized → adjacent segment expansion → mainstream requirements such as stability, trust, safety, support, and monetization.**

Check failure modes: wrong early adopters, MVP validates only a feature not a mechanism, no repeatable proof, manual work cannot be productized, trust/risk lags growth, or mainstream users have higher reliability requirements.

### Project-transfer mapping
When the user asks to combine external cases with their own projects, map by mechanism, not by industry:

**external case mechanism → user’s real project analogue → shared driver point → different constraints → interview-safe expression.**

Example mapping types: recommendation data flywheel ↔ Agent Bad Case knowledge flywheel; early adopter edge market ↔ high-trust/high-value pilot customer; direct chat intent confirmation ↔ GEO high-value question detection; trust governance ↔ article quality/risk review.

## Editing guidance

- Preserve original notes; add analysis sections rather than rewriting the source unless asked.
- Abstract conclusions into reusable questions and mechanisms; do not hard-code one case’s answer as universal truth. For example, write “identify the scarce side” rather than “always prioritize consumers,” and “analyze whether recommendation improves allocation” rather than “recommendation is always better than search.”
- Prefer concise headings, tables, and bullet points.
- Make the final summary memorable as one sentence or one chain.
- For Obsidian notes, link reusable methods to existing notes when obvious, e.g. `[[面试数据飞轮/产品方法论/双边平台冷启动SOP|双边平台冷启动 SOP]]`.
- If creating a new reusable method note, place it under a relevant methodology folder if the vault structure suggests one.

## When more detail is needed

Load only the relevant reference:
- `references/independent-case-sop.md`: full product/company case拆解 from only a product name; includes six mandatory questions, competitor/opportunity branch, post-0-1 development, problems, and solutions.
- `references/product-case-frameworks.md`: detailed perspective library, metrics, decision gates, and mechanism patterns.
- `references/templates.md`: reusable output templates and interview wording.
- `references/iteration-memory.md`: user-aligned decomposition preferences and update protocol; read/update when the user corrects the SOP or asks the skill to learn.
