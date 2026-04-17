# Phase 02 — Research & Insight: PROMPT

## Agent Context

You are assisting with the Research & Insight phase of a physical product development project. Your role is to help the user build an evidence base that reduces uncertainty and supports confident product decisions.

Before beginning, read:
- `../../PROJECT.md` for project identity, vision, and constraints
- `../01-problem-definition/HANDOVER.md` for the problem statement, user profile, and research priorities
- `./BRIEF.md` for this phase's purpose, selected sub-tasks, and done criteria

---

## Sub-Task Prompts

### Competitive Deep-Dive

```
I need a detailed competitive analysis for this product space:

Product: [USER INSERTS DESCRIPTION]
Known competitors from Phase 01: [USER INSERTS LIST]

For each key competitor (top 5-8), analyse:
1. **Product details** — what they sell, key features, materials, quality level
2. **Pricing** — retail price, any tiered offerings, sale patterns
3. **Positioning** — who they target, brand personality, premium vs. value
4. **Strengths** — what they do well, what customers praise
5. **Weaknesses** — what customers complain about, gaps in their offering
6. **Distribution** — where they sell (own site, Amazon, retail, etc.)
7. **Marketing approach** — how they reach customers, social presence, content strategy

Then synthesise:
- Where is the market crowded vs. underserved?
- What's the dominant price/quality tier?
- What would meaningful differentiation look like?
- Are there positioning white spaces?

Use publicly available information. Flag where data is estimated.
```

### User Research Synthesis

```
I need to gather and synthesise user insights for this product:

Product: [USER INSERTS DESCRIPTION]
Target user: [USER INSERTS USER PROFILE FROM PHASE 01]

Research the following sources for user insights:
1. **Customer reviews** of competing products — what do people love and hate?
2. **Forum discussions** — Reddit, niche communities, hobbyist groups
3. **Social media** — what are people saying, sharing, complaining about?
4. **Q&A sites** — what questions are people asking about this category?
5. **YouTube reviews** — what do reviewers praise and criticise?

Synthesise into:
- Top 5 unmet needs or frustrations
- Top 5 things users value most
- Surprising insights — anything unexpected?
- Quotes or sentiments that capture the user's voice (paraphrased)
- Gaps between what manufacturers think matters and what users actually care about
```

### Market Sizing & Segmentation

```
Help me size the market for this product:

Product: [USER INSERTS DESCRIPTION]
Target segment: [USER INSERTS FROM PHASE 01]
Geography: [USER INSERTS TARGET MARKETS]

Provide:
1. **TAM** (Total Addressable Market) — the entire market for this category
2. **SAM** (Serviceable Addressable Market) — the portion reachable with your distribution model
3. **SOM** (Serviceable Obtainable Market) — realistic first-year capture
4. **Methodology** — how you arrived at these numbers, what sources and assumptions
5. **Growth trajectory** — is the market growing, flat, or declining? Key drivers.
6. **Segment validation** — does the target segment from Phase 01 hold up? Are there better or additional segments?

Use ranges, not false precision. Flag confidence levels for each estimate.
```

### Assumption Validation Tracker

```
Here are the top unvalidated assumptions from our Problem Definition phase:

[USER PASTES ASSUMPTION INVENTORY FROM PHASE 01]

For each assumption:
1. What evidence have we gathered (from this phase's research) that validates or invalidates it?
2. Updated status: Validated / Invalidated / Partially Validated / Still Unknown
3. If invalidated — what's the implication? Does it change the problem statement, target user, or viability?
4. If still unknown — what would it take to resolve it? Is it worth pursuing or can we proceed with the risk?

Summarise: Which assumptions have we de-risked? Which remain dangerous? What does this mean for Phase 03?
```

### Materials & Technology Scan

```
For this physical product:

[USER INSERTS PRODUCT DESCRIPTION AND KEY FUNCTIONAL REQUIREMENTS]

Scan available materials and technologies:

1. **Primary materials** — what materials could the main body/structure be made from? Pros/cons/cost of each.
2. **Key components** — any electronic, mechanical, or specialised components needed? Availability, lead times, cost ranges.
3. **Emerging options** — any new materials or technologies that could provide an advantage?
4. **Material constraints** — safety requirements, food contact, skin contact, durability, environmental exposure
5. **Cost drivers** — which material choices most impact unit cost?
6. **Sustainability considerations** — recyclability, sourced materials, eco-certifications available

Organise as a comparison matrix where possible. Flag trade-offs between cost, quality, and manufacturability.
```

### Manufacturing Method Exploration

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION, MATERIALS UNDER CONSIDERATION, ESTIMATED VOLUMES]

Explore feasible manufacturing methods:

1. **Process options** — what manufacturing processes could produce this? (e.g., injection moulding, CNC, PCB assembly, offset printing, die-cutting, etc.)
2. **Volume thresholds** — minimum viable quantities for each process
3. **Tooling requirements** — upfront costs, lead times, modification flexibility
4. **Quality implications** — what does each process mean for tolerances, finish, consistency?
5. **Geographic considerations** — which processes are better sourced domestically vs. overseas?
6. **Prototyping path** — how do you prototype for each manufacturing method before committing to tooling?

Include rough cost ranges where possible. Flag the key decisions that need to be made before committing to a manufacturing path.
```

### Regulatory & Compliance Research

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND TARGET MARKETS]

Research regulatory and compliance requirements:

1. **Mandatory standards** — what safety or performance standards apply? (e.g., CE, UL, FCC, EN71, CPSIA, RoHS, REACH, battery transport regulations)
2. **Testing requirements** — what testing is needed? Estimated cost and timeline.
3. **Labelling requirements** — what must appear on the product or packaging?
4. **Market-specific requirements** — do requirements differ between target markets (EU vs. US vs. UK etc.)?
5. **Age-related requirements** — if applicable, age grading and associated standards
6. **Environmental regulations** — packaging waste directives, WEEE, battery disposal requirements
7. **Certification timeline** — how long does certification take and when in the development process should it be initiated?

Flag any requirements that could significantly impact design, cost, or timeline.
```

### Channel & Distribution Research

```
For this product category:

[USER INSERTS PRODUCT DESCRIPTION AND POSITIONING]

Research distribution channels:

1. **Retail landscape** — which retailers carry this category? What are their buyer requirements (margin, MOQ, packaging, exclusivity)?
2. **Online marketplaces** — Amazon, Etsy, category-specific platforms. Fee structures, competition levels, requirements.
3. **Direct-to-consumer** — own website economics. Customer acquisition costs in this category, fulfilment considerations.
4. **Wholesale/distribution** — do distributors exist for this category? What margins do they require?
5. **Crowdfunding** — is this category suited to Kickstarter/Indiegogo? What's the track record?
6. **International** — shipping, duties, localisation requirements for cross-border sales

For each viable channel:
- Margin requirements
- Minimum requirements to get listed/stocked
- Timeline from approach to shelf
- Typical payment terms
```

### Pricing & Willingness-to-Pay Research

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION, POSITIONING, AND COMPETITIVE LANDSCAPE]

Research pricing dynamics:

1. **Competitor price mapping** — full price landscape of alternatives, organised by tier
2. **Price-feature relationship** — what features or attributes justify higher prices in this category?
3. **Price perception signals** — what do reviews and discussions say about pricing? Where is the "feels expensive" vs. "feels worth it" line?
4. **Channel-specific pricing** — how do prices differ across retail, DTC, Amazon?
5. **Bundle/accessory dynamics** — is there a base + add-on model in this category?
6. **Promotional patterns** — is this category heavily discounted? Seasonal pricing?
7. **Target price range** — based on positioning and competitive landscape, what price range should we target?

Cross-reference with unit economics napkin math from Phase 00. Does the target price support viable margins?
```

### Investment Case Development

```
I'm preparing to seek funding for this product. Here's what I have so far:

Market sizing: [USER INSERTS FROM MARKET SIZING SUB-TASK]
Competitive landscape: [USER INSERTS KEY FINDINGS]
Unit economics: [USER INSERTS FROM PHASE 00 OR PRICING RESEARCH]
Target customer: [USER INSERTS FROM PHASE 01]
Funding path chosen: [USER INSERTS — angel, VC, crowdfunding, grant, etc.]

Help me build the investment case:

1. **Narrative arc** — the compelling story: problem → insight → solution → market → traction → ask
2. **Market opportunity summary** — TAM/SAM/SOM framed for investors (or backers, or grant committees)
3. **Competitive advantage** — what's defensible? Why will you win?
4. **Business model** — how does this make money? Unit economics, margin, path to profitability.
5. **Financial projections** — rough 3-year projection: units, revenue, costs, break-even. (Ranges, not false precision)
6. **Use of funds** — exactly what the money will be spent on and what milestones it unlocks
7. **Risk acknowledgement** — top risks and how they're being mitigated (investors respect honesty)
8. **Ask** — how much, what terms, what the investor/backer gets

Tailor the tone and emphasis for the funding type:
- Angels: emphasise founder, market insight, capital efficiency
- VC: emphasise scale, defensibility, market size (note: rare fit for hardware)
- Crowdfunding: emphasise product story, community, reward value
- Grants: emphasise innovation, impact, feasibility

Flag where the case is weak and what would strengthen it.
```

---

## Synthesis Prompt

```
I've completed the Research & Insight phase. Here are my key outputs:

[USER PASTES KEY FINDINGS FROM WORKBOOK]

Synthesise into a HANDOVER for Phase 03 (Product Definition). I need:

1. Summary of what was researched and the most important findings
2. Updated assumption status — what's validated, what's invalidated, what remains uncertain
3. Key market insights that should drive product decisions
4. Technical/manufacturing feasibility conclusions
5. Competitive positioning opportunity
6. Regulatory or compliance factors that constrain the product
7. Channel and pricing framework
8. Remaining unknowns and risks
9. Confidence rating with justification

Format to match the HANDOVER.md template.
```

---

## Decision Point

At the end of this phase:

- **Proceed** — Research supports the opportunity. Move to Product Definition with an evidence base.
- **Pivot** — Research revealed the original problem/market framing is wrong, but a better direction is clear. Revise and proceed.
- **Return** — Critical assumptions were invalidated. Return to Phase 00 or 01 to reframe.
- **Stop** — Research shows the opportunity is not viable. Archive the project with learnings documented.

Record in DECISIONS.md.

