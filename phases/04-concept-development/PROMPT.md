# Phase 04 — Concept Development: PROMPT

## Agent Context

You are assisting with the Concept Development phase of a physical product development project. Your role is to help generate, explore, and evaluate product concepts that meet the defined requirements.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../03-product-definition/HANDOVER.md` for requirements, specs, design principles, and evaluation criteria
- `./BRIEF.md` for this phase's sub-tasks and done criteria

---

## Sub-Task Prompts

### Concept Ideation

```
I need to generate multiple distinct product concepts for:

Product definition: [USER INSERTS FROM PHASE 03]
Key requirements: [USER INSERTS MUST-HAVES AND TOP SHOULD-HAVES]
Design principles: [USER INSERTS FROM PHASE 03]
Known constraints: [USER INSERTS — cost, size, manufacturing, regulatory]

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

```
I need to evaluate these concepts against our product requirements:

Concepts: [USER INSERTS CONCEPT DESCRIPTIONS]

Evaluation criteria from product definition:
[USER INSERTS CRITERIA — derived from Phase 03 requirements and priorities]

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

```
For this product concept:

[USER INSERTS SELECTED CONCEPT OR CONCEPTS TO EXPLORE]
Use context: [USER INSERTS FROM PHASE 01]
Size/dimension constraints: [USER INSERTS FROM PHASE 03]

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

```
For this product:

[USER INSERTS PRODUCT DESCRIPTION AND BRAND REQUIREMENTS FROM PHASE 03]

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

```
For this product:

Product: [USER INSERTS DESCRIPTION]
Retail/channel requirements: [USER INSERTS FROM PHASE 02/03]
Brand requirements: [USER INSERTS FROM PHASE 03]
Product dimensions (estimated): [USER INSERTS]

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

## Synthesis Prompt

```
I've completed concept development. Here are the concepts explored and evaluation results:

[USER PASTES KEY OUTPUTS]

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

## Decision Point

- **Concept selected** — One primary concept chosen. Proceed to detailed design.
- **Hybrid developed** — Best elements combined from multiple concepts. Proceed.
- **No clear winner** — Concepts are too close or all flawed. Consider more ideation or returning to Phase 03 to sharpen the brief.
- **Concept invalidates definition** — The best concepts don't fit the spec. Return to Phase 03 to adjust.

Record in DECISIONS.md.

