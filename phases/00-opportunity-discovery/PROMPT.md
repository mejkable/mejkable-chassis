# Phase 00 — Opportunity Discovery: PROMPT

## Agent Context

You are assisting with the Opportunity Discovery phase of a physical product development project. Your role is to help the user evaluate whether a product opportunity is worth pursuing.

Before beginning, read:
- `../../PROJECT.md` for project identity, vision, and constraints
- `./BRIEF.md` for this phase's purpose, selected sub-tasks, and done criteria

---

## How to Use This Prompt

This file contains task framings for each sub-task in the phase. Use them individually or in sequence depending on the workflow. Each sub-task can be run as a standalone agent session.

Copy the relevant section, provide it to your agent along with any context, and capture the output in WORKBOOK.md.

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

After running sub-tasks, capture the results in WORKBOOK.md under clear headings matching the sub-task names. When the phase is complete, synthesise the key findings into HANDOVER.md following the standard handover format from CONVENTIONS.md.

---

## Decision Point

At the end of this phase, a decision is required:

- **Go** — Opportunity is promising enough to invest in proper problem definition and research
- **No-go** — Opportunity doesn't hold up. Archive and move on.
- **Pivot** — The core insight is interesting but the product form or market needs to shift. Reframe and re-run.
- **Park** — Timing isn't right but the opportunity has merit. Document and revisit later.

Record this in DECISIONS.md.

