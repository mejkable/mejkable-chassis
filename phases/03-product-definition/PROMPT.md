# Phase 03 — Product Definition: PROMPT

## Agent Context

You are assisting with the Product Definition phase of a physical product development project. Your role is to help translate research insights and problem understanding into a concrete, actionable product specification.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../02-research-insight/HANDOVER.md` for the evidence base
- `../01-problem-definition/HANDOVER.md` for the problem statement and user profile
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
- `../02-research-insight/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
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

### Requirements Definition

**Best format:** Solo with agent, then review with whoever will design or make it
**Solo fallback quality:** High — translating handovers into structured requirements suits the agent; the review catches what the handovers missed.

```
Based on the following project context:

Problem statement: [FROM ../01-problem-definition/HANDOVER.md § Problem Statement — read it, or paste here if you have no file access]
User profile: [FROM ../01-problem-definition/HANDOVER.md § Target User Summary — read it, or paste here if you have no file access]
Key research findings: [FROM ../02-research-insight/HANDOVER.md § Key Findings — read it, or paste here if you have no file access]
Technical feasibility: [FROM ../02-research-insight/HANDOVER.md § Technical / Manufacturing Feasibility — read it, or paste here if you have no file access]
Regulatory requirements: [FROM ../02-research-insight/HANDOVER.md § Regulatory Constraints — read it, or paste here if you have no file access]

Help me define product requirements in three categories:

**Functional requirements** — What must the product DO?
(e.g., "Must accommodate 2-6 players", "Must provide 4+ hours of light per charge", "Must survive a 1m drop")

**Performance requirements** — HOW WELL must it do those things?
(e.g., "Battery must charge in under 3 hours", "Cards must withstand 500+ shuffles", "Flame effect must be visible in daylight")

**Constraints** — What must the product NOT do or exceed?
(e.g., "Must not exceed €45 retail price", "Must not require tools for battery replacement", "Must comply with EN71 toy safety")

For each requirement, note:
- Source (which user need, research finding, or regulation drives it)
- Priority (Must / Should / Could)
- Measurability (how will we verify this is met?)
```

### User Experience Definition

**Best format:** Workshop (2–4 people), or Solo with agent
**Solo fallback quality:** Medium — the journey structure is generic; the specific friction points need people who have watched users.

```
For this product:

[FROM ../02-research-insight/HANDOVER.md § Inputs for Phase 03 and ../01-problem-definition/HANDOVER.md § Target User Summary — read them, or paste here if you have no file access]

Map the complete user experience journey:

1. **Discovery** — How does the user first encounter the product? What catches their attention?
2. **Evaluation** — What do they need to see/know/feel to decide to buy?
3. **Purchase** — Where and how do they buy? What's the transaction experience?
4. **Unboxing/first use** — What's the out-of-box experience? Setup, first impression, learning curve.
5. **Core use** — The primary usage experience. What should it feel like? How long does a typical session last?
6. **Ongoing use** — Repeated use over time. Maintenance, storage, recharging, consumables.
7. **Social/sharing** — How is the experience shared with others? Word of mouth, social media, gifting.
8. **End of life** — What happens when they're done? Disposal, recycling, resale, sentimental keeping.

For each stage, identify:
- The ideal experience
- Potential friction points
- Design implications
```

### Target Specification

**Best format:** Solo with expert review (engineer or manufacturer for the technical rows)
**Solo fallback quality:** Medium — targets without a benchmark unit in hand are Estimated; measure competitors physically where you can.

```
For this product, help me set measurable target specifications:

Product: [FROM ../02-research-insight/HANDOVER.md § Inputs for Phase 03 — read it, or paste here if you have no file access]
Requirements: [FROM ./WORKBOOK.md § Requirements Definition — read it, or paste here if you have no file access]
Competitive benchmarks: [FROM ../02-research-insight/WORKBOOK.md § Competitive Deep-Dive — read it, or paste here if you have no file access]
Cost constraints: [FROM ../02-research-insight/HANDOVER.md § Channel & Pricing Framework — read it, or paste here if you have no file access]

Create a target specification table:

| Attribute | Target | Acceptable Range | Benchmark (best competitor) | Source/Rationale |
|---|---|---|---|---|
| [e.g., Weight] | [e.g., 150g] | [120-180g] | [Competitor X: 200g] | [User need for portability] |

Include categories relevant to this product type:
- Physical: dimensions, weight, materials
- Performance: battery life, durability, capacity, speed
- Quality: finish level, tolerance, consistency
- Cost: COGS target, tooling budget
- Timeline: development milestones, launch target
- Compliance: required certifications and standards
```

### Prioritisation Framework

**Best format:** Workshop (2–4 people)
**Solo fallback quality:** Medium — MoSCoW alone is fast, but the arguments it is meant to surface need more than one voice.

```
Here are the requirements we've defined for this product:

[FROM ./WORKBOOK.md § Requirements Definition — read it, or paste here if you have no file access]

Help me prioritise using MoSCoW:

**Must have** — The product fails without these. Non-negotiable.
**Should have** — Important, expected by users, but the product is viable without them at launch.
**Could have** — Desirable but clearly lower priority. First things to cut if constrained.
**Won't have (this version)** — Explicitly out of scope for V1. May be considered for V2.

For each requirement, justify the priority level. Identify:
- The 3 things most likely to cause arguments (where reasonable people disagree on priority)
- Dependencies (requirements that unlock or block other requirements)
- The "minimum lovable product" — the smallest set of Musts and Shoulds that would still delight the target user
```

### Brand & Identity Requirements

**Best format:** Workshop (2–4 people), or Solo with expert review (designer)
**Solo fallback quality:** Medium — a solo pass produces plausible adjectives; a designer turns them into usable guardrails.

```
For this product:

[FROM ../02-research-insight/HANDOVER.md § Inputs for Phase 03 and ../../PROJECT.md § Product Vision — read them, or paste here if you have no file access; add any existing brand context]

Define the brand and identity requirements:

1. **Brand personality** — 3-5 adjectives that describe how the brand should feel
2. **Visual language direction** — colour palette tendencies, material feel, form language (organic vs geometric, minimal vs ornate, etc.)
3. **Quality signals** — what tells the user "this is a premium/quality/considered product"? (Weight, finish, packaging, details)
4. **Design principles** — 3-5 guiding principles for design decisions (e.g., "simplicity over feature-count", "warmth over clinical", "tactile over visual")
5. **Anti-references** — what should this NOT look or feel like?
6. **Brand consistency needs** — if this is part of a broader brand, what are the non-negotiable brand elements?

These become constraints and guardrails for concept development.
```

### Electronic/Technical Specification

**Best format:** Solo with expert review (electronics engineer)
**Solo fallback quality:** Low — the agent produces a credible outline; component choices, power budgets and safety requirements need an engineer before anything is ordered.

```
For this electronic/technical product:

[FROM ./WORKBOOK.md § Requirements Definition — read it, or paste here if you have no file access]

Help me define the technical specification:

1. **Core electronic components** — LED type/count, microcontroller requirements, sensors, drivers
2. **Power system** — battery type, capacity, charge method, charge time, run time targets
3. **User interface** — controls (buttons, touch, gesture), feedback (light, sound), modes
4. **Connectivity** — if any: Bluetooth, WiFi, NFC — what for and is it truly needed?
5. **Firmware scope** — what does the software need to do? Complexity estimate.
6. **Thermal management** — heat considerations for LEDs, charging, enclosure
7. **Safety requirements** — battery safety, EMC, electrical safety standards
8. **Component availability** — are key components readily available, or are there supply risks?

Flag decisions that need to be made vs. specifications that are already determined.
```

### SKU & Variant Strategy

**Best format:** Solo with agent
**Solo fallback quality:** High — trade-off reasoning the agent handles well; check MOQ implications with a supplier before committing.

```
For this product:

[FROM ../02-research-insight/HANDOVER.md § Inputs for Phase 03 and § Competitive Positioning Opportunity — read them, or paste here if you have no file access]

Help me think through SKU and variant strategy:

1. **Launch SKU count** — how many variants at launch? (Colour, size, edition, bundle)
2. **Variant logic** — what differentiates each variant? (Aesthetic only, functional difference, content difference)
3. **Manufacturing implications** — does each variant need different tooling, packaging, components?
4. **Inventory complexity** — how does variant count affect minimum orders, warehousing, forecasting?
5. **Pricing strategy** — same price across variants, or tiered?
6. **Expansion path** — planned future SKUs? Limited editions? Seasonal variants?
7. **Recommendation** — what's the minimum viable SKU count for launch, and the ideal roadmap?
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
I've completed the Product Definition phase. Here are the key outputs:

[FROM ./WORKBOOK.md, every sub-task output and its footer — read it, or paste here if you have no file access]

Synthesise into a HANDOVER for Phase 04 (Concept Development). I need:

1. Summary of the product definition
2. The prioritised requirements (Must/Should/Could/Won't)
3. Target specification summary
4. Design principles and brand requirements
5. Technical constraints and parameters
6. What concept development is free to explore vs. what is fixed
7. Evaluation criteria for concepts (how will we judge them?)
8. Confidence rating with justification

Format to match the HANDOVER.md template.
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a senior product manager who has shipped physical products and been burned by vague or untestable requirements. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 04 (Concept Development) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Definition locked** — Requirements and specs are clear enough to generate concepts. Proceed.
- **Definition needs input** — Gaps remain that require additional research. Return to Phase 02 for targeted follow-up.
- **Scope adjustment** — The definition reveals the project is bigger/smaller than expected. Adjust scope and re-evaluate.

Record in DECISIONS.md.

