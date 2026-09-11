# Phase 05 — Design Development: PROMPT

## Agent Context

You are assisting with the Design Development phase of a physical product development project. Your role is to help resolve a selected concept into a detailed, buildable design and plan the prototyping path.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../04-concept-development/HANDOVER.md` for the selected concept
- `../03-product-definition/HANDOVER.md` for requirements and specifications
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
- `../04-concept-development/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
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

### Material Specification

**Best format:** Solo with expert review (materials supplier or engineer)
**Solo fallback quality:** Medium — the agent proposes candidates and trade-offs; grades, availability and pricing are Estimated until a supplier confirms.

```
For this product design:

[FROM ../04-concept-development/HANDOVER.md § Selected Concept — read it, or paste here if you have no file access]
Requirements: [FROM ../03-product-definition/HANDOVER.md § Prioritised Requirements — read it, or paste here if you have no file access]
Manufacturing method: [FROM ../02-research-insight/HANDOVER.md § Technical / Manufacturing Feasibility — read it, or paste here if you have no file access]

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

**Best format:** Solo with expert review (manufacturing engineer)
**Solo fallback quality:** Medium — sequence and fastening options are sound; tolerance and fixture reality comes from someone who has assembled similar products.

```
For this product:

[FROM ./WORKBOOK.md § Detailed Design — read it, or paste here if you have no file access]

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

**Best format:** Solo with agent
**Solo fallback quality:** High — systematic checking is what the agent does best; evidence quality depends on the design documentation.

```
Here is the current design and the requirements it must meet:

Design: [FROM ./WORKBOOK.md § Detailed Design — read it, or paste here if you have no file access]
Requirements: [FROM ../03-product-definition/WORKBOOK.md § Requirements Definition — read it, or paste here if you have no file access]

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

**Best format:** Solo with agent, reviewed by whoever will build the prototypes
**Solo fallback quality:** High — roadmap logic suits the agent; lead times and costs are Estimated until quoted.

```
For this product at its current design stage:

[FROM ./WORKBOOK.md § Detailed Design and § Requirements Compliance Review — read them, or paste here if you have no file access; add the key unknowns]

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

**Best format:** Solo with expert review (CMF or industrial designer), with physical samples
**Solo fallback quality:** Low — colour and finish cannot be specified from a description; get swatches and samples.

```
For this product:

[FROM ./WORKBOOK.md § Detailed Design and ../03-product-definition/HANDOVER.md § Design Principles & Brand Requirements — read them, or paste here if you have no file access]

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

**Best format:** Solo with agent, then Solo with expert review (supplier quotes)
**Solo fallback quality:** Medium — structure and cost drivers are right; every unit cost is Estimated until quoted.

```
Based on the current design:

[FROM ./WORKBOOK.md § Bill of Materials (BOM) and § Material Specifications — read them, or paste here if you have no file access; add manufacturing method and estimated volumes]

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

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
Design development is complete. Here are the key outputs:

[FROM ./WORKBOOK.md, every sub-task output and its footer — read it, or paste here if you have no file access]

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

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a DFM engineer who has to make this design in volume and knows what CAD hides. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 06 (Prototyping & Validation) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Design complete** — Ready to prototype. Proceed.
- **Design needs iteration** — Specific issues identified. Iterate within this phase.
- **Design challenges spec** — The design can't meet the spec. Return to Phase 03 to adjust requirements.
- **Cost out of range** — Design is viable but too expensive. Cost-reduction design cycle needed.

