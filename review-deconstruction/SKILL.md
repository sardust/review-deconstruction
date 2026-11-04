---
name: review-deconstruction
description: This skill should be used when the user wants to read, analyze, or "deconstruct" a review/survey paper (综述论文) to learn its writing craft — structure, taxonomy, narrative techniques, figure/table design, and gap-statement construction. Use it when the user says things like "拆解这篇综述", "帮我读这篇 review", "这篇综述怎么写这么好", "分析综述的写法", or is preparing to write their own literature review and wants to learn from exemplars. Not for reading ordinary research papers (that is content reading); this skill is about reverse-engineering how reviews are WRITTEN.
agent_created: true
---

# Review Paper Deconstruction (综述拆解法)

Reverse-engineer how a review/survey paper is written, so the user can extract reusable writing decisions for their own review. Read for **craft**, not content.

Core principle: 读普通论文是"读内容"，读综述是"读写法"（read the craft, not the content）. Every deconstruction must end with concrete decisions: what to copy, what to avoid.

## When to Use

- User provides a review/survey paper (PDF or link) and wants a "拆解" (deconstruction)
- User is writing a literature review and wants to study exemplars before drafting
- User wants to compare several reviews and derive shared writing conventions
- User asks whether a specific review is a good model to imitate

Do NOT use for: summarizing a review's findings (that is content work), or reading ordinary method/experiment papers.

## Workflow

### Step 1 — Confirm the reading mode

State the mode explicitly to the user: this session reads for **writing craft**. Content (facts, benchmarks, references worth adding) is recorded only as a byproduct in the "副产品" section. If the user actually wants a content summary, switch mode instead of mixing.

### Step 2 — First pass: global scan (5–10 min)

Read only: title → abstract → section headings → all figures and tables → conclusion. Build the skeleton before any deep reading:
- Section tree (缩进画出章节树)
- Main line (主线): is it organized by time / by task / by paradigm / mixed?
- Figure/table inventory with one-line function notes

### Step 3 — Second pass: 8-question deconstruction

Walk the 8 questions below. Use `assets/deconstruction-template.md` as the output skeleton (copy it to the user's notes folder, then fill it). Cite concrete evidence (原句/页码/图号) for every claim — a deconstruction without quoted evidence is an opinion, not an analysis.

The 8 questions:

1. **范围界定 (scope)** — Which sentences delimit scope? What is excluded? How are research objectives stated (often "two aims" in the abstract)?
2. **检索方法 (search methodology)** — Is there a dedicated section? Databases, keywords, inclusion criteria, counts, dates, PRISMA-like flow? Is it reproducible? (Many reviews fail here — flag it.)
3. **结构骨架 (structure)** — Section tree; main line type; what question does each major section answer?
4. **分类法 (taxonomy)** — What axes slice the field? Are axes orthogonal? How is the taxonomy figure drawn? What recent dimension is MISSING (e.g., no self-supervised axis)?
5. **叙事技巧 (narrative)** — Sample 3 paragraphs: does each open with a claim sentence? How are transitions made? What follows "然而/however"? Collect reusable sentence patterns (串联句式) verbatim.
6. **图表配置 (figures & tables)** — Count and function of each; do comparison tables carry unified quantitative columns, or only qualitative text?
7. **缺口/展望写法 (challenges & outlook)** — How is the challenge list organized (theme/priority)? Does each challenge carry specific evidence or only vague citations? Is there a roadmap figure?
8. **引用策略 (citation strategy)** — Total reference count; listing style ("one paragraph per study") vs synthesis style (串联式); how are landmark papers cited repeatedly across sections?

### Step 4 — Verdict: copy 3, avoid 2

Fill the final two sections, **concretely**:
- 我要抄的 3 样 — each item = a structural/technique decision with where to apply it in the user's own review
- 它没做好、我要避免的 2 样 — each item = a named flaw with the user's countermeasure

If the review is high quality, still find 2 weaknesses; if low quality, still find 3 strengths. The verdict is what makes the deconstruction actionable — without it the user only learned "what it says", not "how to write".

### Step 5 — Byproduct section (内容性收获)

Record, without letting it dominate: benchmarks/challenges worth citing, references the user's own library may lack, terminology already "occupied" by this review (so the user's framing must differ), and any direct evidence for the user's gap statement (e.g., "this review covers CME detection in only one sentence — my narrow-deep niche is validated").

### Step 6 — Multi-review synthesis (when ≥2 deconstructions exist)

When the user has deconstructed 2+ reviews, load `references/multi-review-synthesis.md` and produce a cross-review decision table: conventions all exemplars share (adopt), flaws all exemplars share (avoid), and axes where exemplars disagree (user must choose deliberately, with reasons tied to their review's goal).

## Output Conventions

- One deconstruction per file: `notes/综述拆解/<编号>_<作者>_<年份>_拆解.md` (or the user's preferred notes layout)
- Keep the filled template under ~200 lines; depth over exhaustiveness
- Language: match the user's language (Chinese for Chinese users), but quote the reviewed paper's original sentences verbatim in the evidence slots
- Always show the user the "copy 3 / avoid 2" verdict inline in chat — that is the highest-signal part

## Quality Bar (self-check before delivering)

- [ ] Section tree drawn with indentation, main line named (time/task/paradigm/mixed)
- [ ] Every "copy/avoid" item tied to quoted evidence or a specific section/figure
- [ ] At least 3 sentence patterns collected verbatim for the user's reusable corpus
- [ ] Verdict is actionable in the user's own outline (references their chapter numbers if known)
- [ ] Byproduct section present but not dominant

## Bundled Resources

- `assets/deconstruction-template.md` — the blank 8-question deconstruction table to copy per review
- `references/worked-example-thaker-2025.md` — a fully worked deconstruction of a mid-quality space-weather AI review, showing both what to copy and what to avoid; use as the gold standard for output quality
- `references/multi-review-synthesis.md` — method for aggregating multiple deconstructions into the user's own writing decision list
