# Phase 03 — Product Definition: PROMPT

## Agent Context

You are assisting with the Product Definition phase of a physical product development project. Your role is to help translate research insights and problem understanding into a concrete, actionable product specification.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../02-research-insight/HANDOVER.md` for the evidence base
- `../01-problem-definition/HANDOVER.md` for the problem statement and user profile
- `./BRIEF.md` for this phase's sub-tasks and done criteria

---

## Sub-Task Prompts

### Requirements Definition

```
Based on the following project context:

Problem statement: [FROM PHASE 01]
User profile: [FROM PHASE 01]
Key research findings: [FROM PHASE 02]
Technical feasibility: [FROM PHASE 02]
Regulatory requirements: [FROM PHASE 02]

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

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND USER PROFILE]

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

```
For this product, help me set measurable target specifications:

Product: [USER INSERTS DESCRIPTION]
Requirements: [USER INSERTS KEY REQUIREMENTS FROM ABOVE]
Competitive benchmarks: [USER INSERTS FROM PHASE 02]
Cost constraints: [USER INSERTS TARGET COGS AND PRICE]

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

```
Here are the requirements we've defined for this product:

[USER INSERTS REQUIREMENTS LIST]

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

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND BRAND CONTEXT]

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

```
For this electronic/technical product:

[USER INSERTS PRODUCT DESCRIPTION AND FUNCTIONAL REQUIREMENTS]

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

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND MARKET POSITIONING]

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

## Synthesis Prompt

```
I've completed the Product Definition phase. Here are the key outputs:

[USER PASTES REQUIREMENTS, SPECS, PRIORITIES, AND OTHER KEY OUTPUTS]

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

## Decision Point

- **Definition locked** — Requirements and specs are clear enough to generate concepts. Proceed.
- **Definition needs input** — Gaps remain that require additional research. Return to Phase 02 for targeted follow-up.
- **Scope adjustment** — The definition reveals the project is bigger/smaller than expected. Adjust scope and re-evaluate.

Record in DECISIONS.md.

