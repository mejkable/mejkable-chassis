# Phase 04 — Concept Development: PROMPT

## Agent Context

You are assisting with the Concept Development phase of a physical product development project. Your role is to help generate, explore, and evaluate product concepts that meet the defined requirements.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../03-product-definition/HANDOVER.md` for requirements, specs, design principles, and evaluation criteria
- `./BRIEF.md` for this phase's purpose, sub-task menu and done criteria
- `./WORKBOOK.md` § Phase Plan for the approved sub-task list, once the Phase Plan prompt below has been run

Work under the Operating Policy in `../../AGENTS.md`: tag every figure, standard, supplier or competitor **Verified**, **Estimated** or **Unknown** and never invent a citation; ask before changing a recorded decision, marking a phase `complete` or committing money; run only the sub-task selected.

---

## How to Use This Prompt

Each sub-task below is a standalone prompt. Run them individually, capture outputs in WORKBOOK.md, and use the synthesis prompt at the end to pull everything together for the HANDOVER. Start with the Phase Plan prompt; run the Critique prompt last, in a fresh session, before the handover is marked final.

### Before you run a sub-task

1. Read the sub-task prompt and its inputs without carrying it out.
2. List what is unclear or missing, in at most five bullets.
3. If any item would materially change the output, ask the user one question and wait for the answer.
4. Otherwise, state your assumptions at the top of the output and proceed.

---

## Phase Plan Prompt

Run this once, at the start of the phase, before any sub-task. Sub-task selection is recorded in WORKBOOK.md, never by editing BRIEF.md.

```
Plan this phase before running any sub-task. Read:
- `../../PROJECT.md`, for identity, constraints, entry point and current status
- `../03-product-definition/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
- `./BRIEF.md`, for the phase purpose, the sub-task menu and the done criteria

Then propose a phase plan:
1. Which sub-tasks to run, from the Core, Conditional and Optional tiers, and in what order
2. For each: one line on why it applies to this project, and the working format you recommend (see the Best format line on each sub-task in PROMPT.md)
3. Which sub-tasks you recommend skipping, and why
4. Anything the done criteria need that the selected sub-tasks do not obviously produce
5. Anything you need from me before starting

Stop and wait for my approval. Once approved, write the agreed list under `## Phase Plan` at the top of `./WORKBOOK.md`, then start with the first sub-task.
```

---

## Sub-Task Prompts

### Concept Ideation

**Best format:** Workshop (3–6 people)
**Solo fallback quality:** Medium — solo generation produces distinct concepts on paper; the range narrows without other minds and without sketching.

```
I need to generate multiple distinct product concepts for:

Product definition: [FROM ../03-product-definition/HANDOVER.md § Product Definition Summary — read it, or paste here if you have no file access]
Key requirements: [FROM ../03-product-definition/HANDOVER.md § Prioritised Requirements — read it, or paste here if you have no file access]
Design principles: [FROM ../03-product-definition/HANDOVER.md § Design Principles & Brand Requirements — read it, or paste here if you have no file access]
Known constraints: [FROM ../03-product-definition/HANDOVER.md § Constraints Established — read it, or paste here if you have no file access]

Generate 4-5 distinct concepts. For each concept:
1. **Concept name** — a short, evocative label
2. **Core idea** — the central organising principle or insight (one sentence)
3. **How it works** — brief description of form, function, and user interaction
4. **Key differentiator** — what makes this concept different from the others
5. **Strengths** — what this concept does particularly well
6. **Weaknesses/risks** — where this concept is vulnerable
7. **Manufacturing implication** — first-pass on how this would be made

The concepts should be meaningfully different — different approaches to the same problem, not just variations on one idea. Include at least one concept that challenges assumptions.
```

### Concept Evaluation Matrix

**Best format:** Solo with agent, scores reviewed by the team
**Solo fallback quality:** High — the matrix is mechanical; contested scores are the point and belong in DECISIONS.md.

```
I need to evaluate these concepts against our product requirements:

Concepts: [FROM ./WORKBOOK.md § Concept Ideation — read it, or paste here if you have no file access]

Evaluation criteria from product definition:
[FROM ../03-product-definition/HANDOVER.md § Inputs for Phase 04, the evaluation criteria — read it, or paste here if you have no file access]

Create an evaluation matrix:

| Criteria | Weight | Concept A | Concept B | Concept C | Concept D |
|---|---|---|---|---|---|
| [Criterion] | [1-5] | [Score 1-5] | [Score 1-5] | [Score 1-5] | [Score 1-5] |

Score each concept 1-5 on each criterion. Weight criteria by importance.

Then provide:
1. Weighted total scores
2. Analysis — where do the concepts cluster? Any surprises?
3. Risk profile comparison — which concept has the best overall risk/reward?
4. Your recommendation and reasoning (but note this is input to a human decision, not the decision itself)
```

### Form Factor Exploration

**Best format:** Solo with expert review (industrial designer), or External tool (sketches, foam or card mock-ups)
**Solo fallback quality:** Low — form is physical; text and renders miss what a rough model shows in five minutes.

```
For this product concept:

Concept(s): [FROM ./WORKBOOK.md § Concept Ideation, the concept or concepts to explore — read it, or paste here if you have no file access]
Use context: [FROM ../01-problem-definition/HANDOVER.md § Target User Summary and § Constraints Established — read them, or paste here if you have no file access]
Size/dimension constraints: [FROM ../03-product-definition/HANDOVER.md § Target Specification Summary — read it, or paste here if you have no file access]

Explore form factor options:

1. **Size variants** — what are the implications of making it larger vs. smaller?
2. **Proportions** — how do different proportions affect function, aesthetics, and manufacturing?
3. **Ergonomics** — how is it held, touched, carried? What does the hand want?
4. **Orientation** — how does it sit, stand, hang, display?
5. **Relationship to environment** — how does it look in context (on a shelf, on a table, in a hand)?
6. **Reference products** — what existing products have gotten form factor right for a similar use case?

Describe 3 form factor directions with rationale for each.
```

### Graphic & Visual Design Concepts

**Best format:** Solo with expert review (graphic designer), or External tool (image generation, mood boards)
**Solo fallback quality:** Medium — directions in words are useful for briefing; they are not designs.

```
For this product:

[FROM ../03-product-definition/HANDOVER.md § Product Definition Summary and § Design Principles & Brand Requirements — read them, or paste here if you have no file access]

Explore graphic and visual design directions:

1. **Style direction A** — describe a visual approach: illustration style, colour palette, typography, overall mood
2. **Style direction B** — a meaningfully different approach
3. **Style direction C** — a third option, perhaps more unexpected

For each direction:
- Mood/reference description (describe what existing work or styles it draws from)
- How it serves the brand personality
- How it resonates with the target user
- Production implications (print complexity, colour count, special finishes)
- Strengths and risks

Note: if artwork/content is coming as input to the project, focus on packaging, branding, and peripheral visual design.
```

### Packaging Concept Development

**Best format:** Solo with agent, then Solo with expert review (packaging supplier)
**Solo fallback quality:** Medium — structural options and cost tiers are well covered; dielines and real costs need a supplier.

```
For this product:

Product: [FROM ../03-product-definition/HANDOVER.md § Product Definition Summary — read it, or paste here if you have no file access]
Retail/channel requirements: [FROM ../02-research-insight/HANDOVER.md § Channel & Pricing Framework — read it, or paste here if you have no file access]
Brand requirements: [FROM ../03-product-definition/HANDOVER.md § Design Principles & Brand Requirements — read it, or paste here if you have no file access]
Product dimensions (estimated): [FROM ../03-product-definition/HANDOVER.md § Target Specification Summary — read it, or paste here if you have no file access]

Develop packaging concepts:

1. **Structural concepts** — box type, closure method, inserts, window/no window, materials
2. **Unboxing experience** — what happens when the customer opens it? Sequence of reveal.
3. **Retail shelf presence** — how does it stand out? Face-out vs. spine. Hang-tag vs. shelf.
4. **Shipping considerations** — does retail packaging also serve as shipping packaging? Over-box needed?
5. **Sustainability options** — plastic-free? Recyclable? Minimal waste?
6. **Cost tiers** — basic, mid, premium packaging — what does each level look like and cost?
7. **Information hierarchy** — what goes on front, back, sides? What must be there (regulatory) vs. what should be?

Recommend a packaging direction that balances brand experience, cost, and practical requirements.
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
I've completed concept development. Here are the concepts explored and evaluation results:

[FROM ./WORKBOOK.md, every sub-task output and its footer — read it, or paste here if you have no file access]

Synthesise into a HANDOVER for Phase 05 (Design Development). I need:

1. Summary of concepts explored and selection rationale
2. Selected concept description (comprehensive)
3. Key design parameters established
4. What remains to be resolved in design development
5. Elements from rejected concepts worth preserving
6. Risk areas in the selected concept
7. Confidence rating with justification
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a design director who has seen many concepts chosen for the wrong reasons. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 05 (Design Development) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Concept selected** — One primary concept chosen. Proceed to detailed design.
- **Hybrid developed** — Best elements combined from multiple concepts. Proceed.
- **No clear winner** — Concepts are too close or all flawed. Consider more ideation or returning to Phase 03 to sharpen the brief.
- **Concept invalidates definition** — The best concepts don't fit the spec. Return to Phase 03 to adjust.

Record in DECISIONS.md.

