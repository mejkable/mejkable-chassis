# Phase 00 — Opportunity Discovery: PROMPT

## Agent Context

You are assisting with the Opportunity Discovery phase of a physical product development project. Your role is to help the user evaluate whether a product opportunity is worth pursuing.

Before beginning, read:
- `../../PROJECT.md` for project identity, vision, and constraints
- `./BRIEF.md` for this phase's purpose, sub-task menu and done criteria
- `./WORKBOOK.md` § Phase Plan for the approved sub-task list, once the Phase Plan prompt below has been run

Work under the Operating Policy in `../../AGENTS.md`: tag every figure, standard, supplier or competitor **Verified**, **Estimated** or **Unknown** and never invent a citation; ask before changing a recorded decision, marking a phase `complete` or committing money; run only the sub-task selected.

---

## How to Use This Prompt

This file contains task framings for each sub-task in the phase. Use them individually or in sequence depending on the workflow. Each sub-task can be run as a standalone agent session.

Copy the relevant section, provide it to your agent along with any context, and capture the output in WORKBOOK.md.

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
- Pre-existing Inputs under Entry Point in `../../PROJECT.md`, for whatever the project already brings
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

### Opportunity Framing

```
I have an idea for a physical product. Here's what I'm thinking:

[USER INSERTS DESCRIPTION]

Help me articulate this opportunity clearly. I need:
1. A one-paragraph opportunity statement — what is the product, who is it for, and why does it matter
2. What assumptions am I making (list them explicitly)
3. What's the strongest version of this idea, and what's the weakest version
4. Three questions I should answer before going further

Keep it direct. Don't pad or flatter — I need honest assessment.
```

### Initial Market Scan

```
I'm evaluating an opportunity in the following space:

[USER INSERTS OPPORTUNITY STATEMENT OR DESCRIPTION]

Conduct a first-pass market scan. I need:
1. Market overview — is this an existing category or a new one? Estimated size if possible.
2. Key existing players — who's already selling something similar or adjacent? (names, price points, positioning)
3. Market direction — growing, flat, or declining? Any signals?
4. Obvious gaps — what's missing from current offerings?
5. Barriers to entry — what makes this hard to enter?

Focus on publicly available information. Flag where you're uncertain or estimating.
```

### Target Customer Sketch

```
For this product opportunity:

[USER INSERTS OPPORTUNITY STATEMENT]

Create a first-pass customer sketch. I need:
1. Primary customer segment — who is most likely to buy this? Demographics, psychographics, buying behaviour.
2. What problem or desire drives them — why would they want this?
3. Where they currently shop for similar products — channels, platforms, stores
4. What they currently use instead — direct substitutes and workarounds
5. Willingness to pay — any signals on price sensitivity for this segment?

This is a rough sketch, not a research report. Flag your assumptions.
```

### Founder-Market Fit Check

```
I'm evaluating whether I/we are the right team for this opportunity.

The opportunity: [USER INSERTS DESCRIPTION]

My/our background and capabilities: [USER INSERTS RELEVANT EXPERIENCE, SKILLS, RESOURCES]

Help me assess:
1. What advantages do I/we have in pursuing this?
2. What critical gaps exist in skills, knowledge, or resources?
3. Are the gaps fillable (hire, learn, partner) or structural blockers?
4. Honest assessment — is this a strong fit, workable fit, or poor fit?
```

### Trend & Timing Analysis

```
For this product opportunity:

[USER INSERTS DESCRIPTION]

Analyse timing and trends:
1. What cultural, technological, or market trends support this now?
2. Is there a "why now" catalyst — new technology, regulation change, cultural shift?
3. What's the risk of being too early or too late?
4. Any seasonal or cyclical factors relevant to launch timing?
```

### Unit Economics Napkin Math

```
I need a very rough first-pass on unit economics for this product:

[USER INSERTS PRODUCT DESCRIPTION, ANY KNOWN COST DATA]

Help me estimate:
1. Likely COGS range (materials, manufacturing, packaging) — use comparable products as benchmarks if specific data isn't available
2. Target retail / selling price range based on market positioning
3. Gross margin estimate
4. Key cost drivers that could swing the margin significantly
5. Minimum order quantity considerations
6. Red flags — anything that makes the economics obviously unworkable?

This is napkin math. Use ranges, not false precision. Flag all assumptions.
```

### Risk Flags

```
Evaluate the key risks for this product opportunity:

[USER INSERTS DESCRIPTION AND ANY CONTEXT FROM OTHER SUB-TASKS]

Identify:
1. Technical risks — can this actually be built/manufactured?
2. Market risks — does demand actually exist?
3. Financial risks — capital requirements, cash flow, break-even timeline
4. Competitive risks — what could a larger player do?
5. Regulatory risks — anything that could block or delay?
6. Single points of failure — what, if it goes wrong, kills the whole project?

Rate each as High / Medium / Low impact and likelihood. Focus on the ones that matter most.
```

### Funding Path Assessment

```
I'm evaluating how to fund this product opportunity:

Product opportunity: [USER INSERTS DESCRIPTION]
Estimated capital requirements: [USER INSERTS — rough range from unit economics, or "unknown"]
Available personal/team resources: [USER INSERTS — savings, revenue from existing business, available investment]
Timeline: [USER INSERTS — how fast does this need to move?]

Help me assess funding options:

1. **Bootstrapping** — can this be self-funded? What's the minimum viable investment to get to revenue? What are the constraints (slower timeline, smaller first run, limited marketing)?
2. **Crowdfunding (Kickstarter/Indiegogo)** — is this product suited to crowdfunding? What's the category track record? What would a realistic campaign target be? What's needed to run a successful campaign?
3. **Angel investment** — is this the right scale and type for angels? What would an angel expect in return? How much could you realistically raise?
4. **VC funding** — is this a VC-scale opportunity? (Most physical products aren't — be honest.) What would a VC need to see?
5. **Grants & competitions** — are there relevant innovation grants, design awards with funding, or startup competitions?
6. **Pre-orders / revenue funding** — can early sales fund production? What are the risks?
7. **Recommended path** — given the opportunity, capital needs, and team situation, what's the most realistic and appropriate funding approach?
8. **Key milestones before funding** — what should be done BEFORE approaching investors or launching a campaign?

Be realistic. Most hardware products are best served by bootstrapping or crowdfunding. VC is rarely appropriate for physical products unless there's a tech/platform play.
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the handover synthesis reads from them. When the phase closes, synthesise the key findings into HANDOVER.md following the handover format in `config/CONVENTIONS.md`.

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are an experienced hardware investor who has seen many opportunity pitches fail. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 01 (Problem Definition) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

At the end of this phase, a decision is required:

- **Go** — Opportunity is promising enough to invest in proper problem definition and research
- **No-go** — Opportunity doesn't hold up. Archive and move on.
- **Pivot** — The core insight is interesting but the product form or market needs to shift. Reframe and re-run.
- **Park** — Timing isn't right but the opportunity has merit. Document and revisit later.

Record this in DECISIONS.md.

