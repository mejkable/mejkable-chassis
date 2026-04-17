# Phase 05 — Design Development: PROMPT

## Agent Context

You are assisting with the Design Development phase of a physical product development project. Your role is to help resolve a selected concept into a detailed, buildable design and plan the prototyping path.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../04-concept-development/HANDOVER.md` for the selected concept
- `../03-product-definition/HANDOVER.md` for requirements and specifications
- `./BRIEF.md` for this phase's sub-tasks and done criteria

---

## Sub-Task Prompts

### Material Specification

```
For this product design:

[USER INSERTS DESIGN DESCRIPTION AND KEY COMPONENTS]
Requirements: [USER INSERTS RELEVANT REQUIREMENTS — durability, safety, cost, feel, appearance]
Manufacturing method: [USER INSERTS EXPECTED MANUFACTURING APPROACH]

Help me specify materials for each component:

| Component | Material Options | Recommended | Rationale | Cost Impact | Supplier Notes |
|---|---|---|---|---|---|
| | | | | | |

For each recommendation, address:
1. Does it meet safety/regulatory requirements?
2. Is it available in the quantities we need?
3. How does it affect manufacturing (mouldability, printability, workability)?
4. What does it feel like to the user (tactile quality, weight, temperature)?
5. Environmental/sustainability profile
6. Any supply chain risks?
```

### Assembly & Construction Planning

```
For this product:

[USER INSERTS DESIGN WITH COMPONENT LIST]

Plan the assembly:

1. **Bill of Materials (BOM)** — complete list of parts, quantities, materials, and sources
2. **Assembly sequence** — step-by-step order of assembly. What goes together first?
3. **Fastening methods** — how parts join: snap-fits, screws, adhesive, ultrasonic welding, press-fit, etc.
4. **Critical interfaces** — where do parts meet? What tolerances matter?
5. **Assembly complexity** — estimated time, skill required, tools needed
6. **Quality checkpoints** — where in assembly should quality be verified?
7. **Packaging into box** — how does the assembled (or unassembled) product get into packaging?

Flag any assembly steps that are high-risk, slow, or require special skills/equipment.
```

### Design Review Against Requirements

```
Here is the current design and the requirements it must meet:

Design: [USER INSERTS DESIGN DESCRIPTION OR SPECIFICATION]
Requirements: [USER INSERTS FULL REQUIREMENTS LIST FROM PHASE 03]

Conduct a systematic design review:

| Requirement | Priority | Met? | How / Evidence | Notes |
|---|---|---|---|---|
| | Must/Should/Could | Yes/Partial/No/Untested | | |

Identify:
1. Any Must-Have requirements not yet met — these are blockers
2. Any Should-Have requirements traded off — document the trade-off
3. Requirements that can only be verified through prototyping — carry to Phase 06
4. Any new requirements discovered during design that weren't in the original spec
```

### Prototyping Strategy

```
For this product at its current design stage:

[USER INSERTS DESIGN DESCRIPTION AND KEY UNKNOWNS]

Help me plan a prototyping roadmap:

1. **What needs to be tested** — list the key questions/risks that prototyping must answer
2. **Prototype types needed:**
   - Looks-like prototype (appearance, form, finish — but not functional)
   - Works-like prototype (functional — but may not look final)
   - Works-like-looks-like prototype (integrated — close to final)
3. **For each prototype:**
   - Purpose (what question does it answer?)
   - Method (3D print, handmade, breadboard, short-run production, etc.)
   - Fidelity level (rough/medium/high)
   - Estimated cost and lead time
   - What "success" looks like for this prototype
4. **Sequence** — which prototypes first? What gates between them?
5. **Prototype-to-production gap** — what won't the prototype tell us that only production samples will?
```

### CMF Specification (Colour, Material, Finish)

```
For this product:

[USER INSERTS DESIGN AND BRAND DIRECTION]

Develop the CMF specification:

1. **Colours** — specific colour definitions (Pantone, RAL, or custom). Primary, secondary, accent.
2. **Materials** — surface material for each visible component (linked to material spec)
3. **Finishes** — surface treatment for each component: matte, gloss, soft-touch, textured, brushed, polished, etc.
4. **Print/marking** — any printing, embossing, debossing, laser marking on the product
5. **Tactile experience** — how does each surface feel? Weight perception.
6. **Manufacturing implications** — how does each CMF choice affect production cost and process?
7. **Consistency requirements** — colour matching between components, batch-to-batch consistency

Present as a CMF board/specification that could be shared with a manufacturer.
```

### Cost Engineering

```
Based on the current design:

[USER INSERTS BOM, MATERIALS, MANUFACTURING METHOD, ESTIMATED VOLUMES]

Build a detailed cost estimate:

| Cost Element | Unit Cost | Quantity | Total per Unit | Notes |
|---|---|---|---|---|
| Materials | | | | |
| Components | | | | |
| Manufacturing labour | | | | |
| Tooling (amortised) | | | | |
| Assembly | | | | |
| Packaging | | | | |
| Testing/QC | | | | |
| Freight/shipping | | | | |
| **Total COGS** | | | | |

Compare to target COGS from Phase 03. If over target:
- Where are the biggest cost drivers?
- What are the cost reduction opportunities?
- What's the impact on margin at target retail price?
```

---

## Synthesis Prompt

```
Design development is complete. Here are the key outputs:

[USER PASTES KEY SPECIFICATIONS, BOM, COST ESTIMATE, PROTOTYPE PLAN]

Synthesise into a HANDOVER for Phase 06 (Prototyping & Validation). Include:
1. Design summary and key specifications
2. BOM overview
3. Prototyping roadmap
4. Requirements compliance status
5. Cost position vs. target
6. Key risks going into prototyping
7. Confidence rating
```

---

## Decision Point

- **Design complete** — Ready to prototype. Proceed.
- **Design needs iteration** — Specific issues identified. Iterate within this phase.
- **Design challenges spec** — The design can't meet the spec. Return to Phase 03 to adjust requirements.
- **Cost out of range** — Design is viable but too expensive. Cost-reduction design cycle needed.

