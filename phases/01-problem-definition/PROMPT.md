# Phase 01 — Problem Definition: PROMPT

## Agent Context

You are assisting with the Problem Definition phase of a physical product development project. Your role is to help the user sharpen a broad opportunity into a specific, well-framed problem that can drive product decisions.

Before beginning, read:
- `../../PROJECT.md` for project identity, vision, and constraints
- `../00-opportunity-discovery/HANDOVER.md` for what's known so far
- `./BRIEF.md` for this phase's purpose, selected sub-tasks, and done criteria

---

## How to Use This Prompt

Each sub-task below is a standalone prompt. Run them individually, feed outputs into WORKBOOK.md, and use the synthesis prompt at the end to pull everything together for the HANDOVER.

---

## Sub-Task Prompts

### Problem Statement Drafting

```
Based on the following opportunity context:

[USER INSERTS PHASE 00 HANDOVER OR OPPORTUNITY DESCRIPTION]

Help me draft a clear problem statement. Use this structure:

1. **Who** has the problem (specific person or segment, not "people")
2. **What** is the problem (observable behaviour, unmet need, or frustration)
3. **Where/when** does it occur (context, environment, situation)
4. **Why** it matters (consequences of it going unsolved — functional, emotional, financial)
5. **How** it's currently dealt with (existing alternatives and their shortcomings)

Then write a single-paragraph problem statement that integrates all five elements.

Finally, challenge the statement:
- Is this a real problem or a solution looking for a problem?
- Is it specific enough to design against?
- Could two different people read this and imagine roughly the same product direction?
```

### User/Customer Deep-Dive

```
I'm developing a physical product and need to understand my target user better.

The product opportunity: [USER INSERTS DESCRIPTION]
What I know so far about the user: [USER INSERTS PHASE 00 CUSTOMER SKETCH OR CURRENT KNOWLEDGE]

Help me build a deeper user profile:

1. **Demographics** — age range, income, location, household composition (only what's relevant)
2. **Psychographics** — values, lifestyle, identity, what they care about
3. **Buying behaviour** — where they shop, how they discover products, impulse vs. considered purchase, price sensitivity
4. **Relationship to the problem** — how aware are they of the problem? Do they actively seek solutions or cope passively?
5. **User vs. buyer distinction** — is the person using this the same person buying it? If not, map both.
6. **Day-in-the-life sketch** — a brief narrative of when and how this product enters their life

Flag where you're making assumptions vs. working from data.
```

### Jobs-to-be-Done Mapping

```
For this product and user:

Product: [USER INSERTS DESCRIPTION]
Target user: [USER INSERTS USER PROFILE OR SUMMARY]

Map the jobs-to-be-done:

1. **Functional jobs** — What practical task are they trying to accomplish? (e.g., "make better coffee at home than a café")
2. **Emotional jobs** — How do they want to feel? (e.g., "feel calm and intentional in the morning")
3. **Social jobs** — How do they want to be perceived? (e.g., "have a kitchen that looks curated")
4. **Related jobs** — What adjacent tasks happen before, during, or after the core job? (e.g., "build a ritual around starting the day")

For each job:
- Rate importance to the user (High / Medium / Low)
- Rate how well current alternatives satisfy it (Well / Partially / Poorly)
- The sweet spot is High importance + Poorly satisfied

Identify the top 2-3 jobs the product must nail.
```

### Current Alternatives Analysis

```
For this problem space:

[USER INSERTS PROBLEM STATEMENT OR DESCRIPTION]

Map the competitive alternatives landscape:

1. **Direct alternatives** — Products that solve the same problem the same way (direct competitors)
2. **Indirect alternatives** — Products that solve the same problem differently
3. **Non-consumption** — People who live with the problem unsolved. Why?
4. **DIY/workarounds** — Makeshift solutions people have cobbled together

For each alternative:
- What it does well
- Where it falls short
- Price point
- Where it's sold
- User sentiment (if you can infer from reviews, forums, etc.)

Identify the gap — what's the unmet need that existing alternatives don't cover?
```

### Assumption Inventory

```
Based on everything we've developed so far in this project:

[USER INSERTS RELEVANT CONTEXT — PROBLEM STATEMENT, USER PROFILE, JTBD, ALTERNATIVES]

Create an assumption inventory. List every assumption embedded in our thinking, then categorise each:

| Assumption | Category | Status | Risk if Wrong | How to Validate |
|---|---|---|---|---|
| [Assumption] | Market / User / Technical / Financial / Channel | Validated / Guess / Unknown | High / Medium / Low | [Method] |

Categories:
- **Market** — assumptions about market size, growth, timing
- **User** — assumptions about who the user is, what they want, how they behave
- **Technical** — assumptions about what's buildable, manufacturable, feasible
- **Financial** — assumptions about costs, pricing, margins
- **Channel** — assumptions about how the product reaches the customer

Flag the top 5 assumptions that are both high-risk and unvalidated. These become the priority research agenda for Phase 02.
```

### Use Context Mapping

```
For this physical product:

[USER INSERTS PRODUCT AND USER DESCRIPTION]

Map the use context in detail:

1. **Physical environment** — Where is this product used? Indoor/outdoor? Size of space? Lighting? Temperature? Moisture? (Hardware products live in the real world — this drives material and form decisions)
2. **Social context** — Used alone or with others? Private or public? Does it need to look good or just work?
3. **Temporal context** — How often? How long each use? Seasonal? Daily ritual? One-time setup?
4. **Adjacent objects** — What's around it? What does it sit on, next to, or interact with?
5. **Handling and interaction** — How do people physically interact? Hands? Tools? One hand or two? Standing or sitting?
6. **Storage and transport** — Where does it live when not in use? Does it travel?
7. **Lifecycle context** — How long should it last? Is it precious or disposable? Will it be gifted or resold?

Identify any context factors that should become hard design constraints.
```

### Stakeholder Mapping

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND TARGET USER]

Map all stakeholders beyond the end user:

1. **Buyer** (if different from user) — What are their criteria? What convinces them?
2. **Influencers** — Who recommends or reviews? Friends, family, online communities, media?
3. **Retailers/distributors** — If this goes through retail, what do they care about? (margin, shelf space, packaging, returns)
4. **Gift-givers** — If this is a gift product, what matters? (presentation, price perception, universality)
5. **Adjacent users** — Others who experience the product (e.g., guests in a host's home, family members witnessing a daily routine, co-players in a game)
6. **Regulators** — Any certification bodies, safety standards, or compliance gatekeepers?
7. **Suppliers/manufacturers** — Their constraints become your constraints

For each stakeholder: what do they need, and what power do they have over the product's success?
```

### Emotional/Aspirational Dimension

```
For this product and user:

[USER INSERTS PRODUCT AND USER DESCRIPTION]

Explore the emotional and aspirational layer:

1. What does the user want to **feel** when using/owning this product?
2. What does it **say about them** to others?
3. What **identity** does it reinforce or help them express?
4. What's the **emotional gap** in current alternatives? (They work functionally but feel ___?)
5. Are there **rituals** associated with this product category? (Lighting a candle, unboxing a game, etc.)
6. What **sensory qualities** matter? (Touch, weight, sound, smell, visual appeal)

How should these emotional dimensions influence design decisions?
```

### Gift & Occasion Mapping

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION]

Assess the gift and occasion potential:

1. **Self-purchase vs. gift split** — What percentage of sales might be gifts? What drives each?
2. **Key occasions** — birthdays, holidays, housewarmings, hostess gifts, "just because"?
3. **Seasonal concentration** — Is demand likely to spike at certain times of year?
4. **Gift requirements** — What does a product need to be gift-worthy? (Packaging, price point, presentation, universality)
5. **Unboxing experience** — How important is the reveal moment?
6. **Price perception** — Does the product need to feel like it costs what it costs? (Gift products often need to "look the price")

How should gift/occasion dynamics influence packaging, pricing, and launch timing?
```

---

## Synthesis Prompt

Run this after completing the sub-tasks above to prepare the HANDOVER.

```
I've completed the Problem Definition phase. Here are my outputs:

[USER PASTES KEY OUTPUTS FROM WORKBOOK]

Help me synthesise this into a HANDOVER for the next phase (Research & Insight). I need:

1. A 2-3 sentence summary of the problem definition work
2. The refined problem statement
3. The prioritised jobs-to-be-done (top 3)
4. The user profile summary
5. Top 5 unvalidated assumptions to test in Phase 02
6. Key constraints established
7. Open questions to carry forward
8. A confidence rating (High/Medium/Low) with justification

Format this to match the HANDOVER.md template.
```

---

## Decision Point

At the end of this phase, confirm:

- **Problem confirmed** — The problem is real, specific, and worth solving. Proceed to Research.
- **Problem reframed** — The original framing was off. A better problem has been identified. Update and proceed.
- **Problem insufficient** — Can't define a clear enough problem. Return to Phase 00 or abandon.

Record in DECISIONS.md.

