# Phase 07 — Production Development: PROMPT

## Agent Context

You are assisting with the Production Development phase. Your role is to help navigate manufacturing decisions, supplier evaluation, quality planning, and production logistics.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../06-prototyping-validation/HANDOVER.md` for frozen design and production inputs
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
- `../06-prototyping-validation/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
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

### Supplier Selection & Evaluation

**Best format:** Solo with agent for the framework, then Primary research (RFQs to 3–5 suppliers)
**Solo fallback quality:** Medium — scorecards and RFQ templates are solid; supplier quality is only visible through quotes, samples and calls.

```
I need to evaluate and select manufacturers for this product:

Product: [FROM ../06-prototyping-validation/HANDOVER.md § Inputs for Phase 07 — read it, or paste here if you have no file access]
BOM: [FROM ../05-design-development/WORKBOOK.md § Bill of Materials (BOM) — read it, or paste here if you have no file access]
Volume: [USER PROVIDES: initial and annual volume estimates]
Location preference: [Domestic / Overseas / No preference]
Budget: [FROM ../05-design-development/HANDOVER.md § Cost Position — read it, or paste here if you have no file access]

Help me:

1. **Evaluation criteria** — what factors should I score suppliers on? Create a weighted scorecard.
   (Quality, price, MOQ, lead time, communication, location, experience, capacity, IP protection, payment terms, certifications)

2. **Supplier outreach template** — draft an RFQ (request for quote) that covers everything a supplier needs to quote accurately.

3. **Red flags to watch for** — what are warning signs when evaluating a new supplier?

4. **Comparison framework** — once quotes come back, how to compare them fairly (not just on unit price).

5. **Negotiation points** — what's typically negotiable and what levers exist?

6. **Contract essentials** — key terms that must be in the manufacturing agreement.
```

### DFM Review Preparation

**Best format:** Solo with expert review (the manufacturer's engineer)
**Solo fallback quality:** Medium — the checklist prepares you well; the review itself is theirs.

```
I'm preparing for a DFM (Design for Manufacturing) review with my manufacturer:

Design: [FROM ../06-prototyping-validation/HANDOVER.md § Final Design Status — read it, or paste here if you have no file access]
Manufacturing process: [USER PROVIDES: e.g. injection moulding, PCB assembly, offset print]
Known concerns: [FROM ../06-prototyping-validation/HANDOVER.md § Key Learnings and § Open Questions — read them, or paste here if you have no file access]

Help me prepare:

1. **DFM checklist by process** — common manufacturability issues for this process type
2. **Questions to ask the manufacturer** — what should I ask them to evaluate?
3. **Common DFM changes** — typical modifications manufacturers request and their impact
4. **Red lines** — design elements that should NOT change even if the manufacturer suggests it (tied to requirements)
5. **Documentation to provide** — what files and specs does the manufacturer need for a thorough DFM review?

After the DFM review, help me evaluate proposed changes:
| Proposed Change | Reason | Impact on Design | Impact on Cost | Impact on Quality | Accept? |
|---|---|---|---|---|---|
```

### Quality Plan Development

**Best format:** Solo with expert review (QC or sourcing specialist)
**Solo fallback quality:** Medium — AQL levels and inspection structure are standard; defect definitions for your product need someone who has inspected similar ones.

```
I need a quality plan for manufacturing this product:

Product: [FROM ../06-prototyping-validation/HANDOVER.md § Inputs for Phase 07 — read it, or paste here if you have no file access]
Key quality requirements: [FROM ../03-product-definition/HANDOVER.md § Prioritised Requirements and § Target Specification Summary — read them, or paste here if you have no file access]
Manufacturing process: [USER PROVIDES: the selected process]
Volume: [USER PROVIDES: order quantity]

Help me develop:

1. **Incoming quality control** — what checks on raw materials and components?
2. **In-process quality control** — what checks during manufacturing?
3. **Final quality control** — what checks on finished product?
4. **AQL (Acceptable Quality Level)** — recommended AQL levels by defect severity:
   - Critical defects (safety, function failure): AQL = [recommend]
   - Major defects (significant cosmetic, minor function): AQL = [recommend]
   - Minor defects (cosmetic only): AQL = [recommend]
5. **Inspection protocol** — how to conduct inspection, sampling method, tools needed
6. **Defect classification guide** — visual and functional standards: what's acceptable vs. rejected
7. **Golden sample** — define the reference standard all production is measured against
8. **Corrective action process** — what happens when quality issues are found?
```

### Production Costing

**Best format:** Solo with agent, over real quotes
**Solo fallback quality:** High — the model is mechanical; every input must be a quote, not an estimate, or the output inherits the Estimated tag.

```
Help me build a comprehensive landed cost model:

BOM: [FROM ../05-design-development/WORKBOOK.md § Bill of Materials (BOM) — read it, or paste here if you have no file access]
Manufacturing cost: [FROM ./WORKBOOK.md § Supplier Evaluation, the selected quote — read it, or paste here if you have no file access]
Tooling: [FROM ./WORKBOOK.md § Supplier Evaluation, the tooling quote — read it, or paste here if you have no file access]
Volume: [USER PROVIDES: order quantity]

Calculate:

| Cost Element | Per Unit | Total (first run) | Notes |
|---|---|---|---|
| Raw materials / components | | | |
| Manufacturing / assembly | | | |
| Tooling (amortised over run) | | | |
| Packaging materials | | | |
| Packaging assembly | | | |
| Quality inspection | | | |
| Compliance testing (amortised) | | | |
| Freight (factory to warehouse) | | | |
| Customs duties / tariffs | | | |
| Insurance | | | |
| Warehousing | | | |
| **Total landed COGS** | | | |

Then analyse:
- Margin at target retail price
- Break-even volume
- Sensitivity: what if volume is 50% lower or 200% higher?
- Biggest cost reduction opportunities
- Cash flow: when does money go out vs. come in?
```

### Production Timeline

**Best format:** Solo with agent, checked against supplier-confirmed lead times
**Solo fallback quality:** Medium — the structure is standard; every duration is Estimated until a supplier confirms it.

```
Help me build a production timeline for:

Product: [FROM ../06-prototyping-validation/HANDOVER.md § Inputs for Phase 07 — read it, or paste here if you have no file access]
Target launch date: [USER PROVIDES: target launch date, or "help me determine"]
Key milestones known: [USER PROVIDES: e.g. tooling already ordered]

Map the timeline:

1. **Tooling / setup** — order, manufacture, trial, approval
2. **Material sourcing** — lead times for key materials/components
3. **Pre-production samples** — production, review, approval cycles
4. **Certification / testing** — submission, testing, certification receipt
5. **Mass production** — production run duration
6. **Quality inspection** — pre-shipment inspection
7. **Shipping** — factory to warehouse, customs clearance
8. **Warehouse receiving** — quality check, inventory logging
9. **Ready for sale** — when can the first unit ship to a customer?

Include buffer time for common delays. Flag critical path items — what delays cascade?
Work backwards from launch date to determine when each step must begin.
```

### Production Funding Execution

**Best format:** Solo with expert review (someone who has run a campaign or closed a round)
**Solo fallback quality:** Medium — the plan structure is sound; execution details and realistic targets need experience.

```
I need to fund production for this product:

Total capital required (FROM ./WORKBOOK.md § Production Costing — read it, or fill in below if you have no file access):
- Tooling:
- First production run:
- Packaging:
- Certification/testing:
- Freight & logistics:
- Buffer/contingency:
- **Total:**

Funding path chosen: [FROM ../00-opportunity-discovery/DECISIONS.md or ../02-research-insight/DECISIONS.md, the funding path decision — read it, or paste here if you have no file access]
Production timeline: [FROM ./WORKBOOK.md § Production Timeline — read it, or paste here if you have no file access]
Cash available now: [USER PROVIDES: cash available now]

Help me build a funding execution plan:

1. **Cash flow timeline** — when does each cost hit? Map money-out against the production timeline.
2. **Funding timeline** — when must funding be secured to avoid delaying production? Work backwards from first payment due.
3. **If crowdfunding:**
   - Campaign target (total needed + platform fees + fulfilment buffer)
   - Campaign timeline aligned with production timeline
   - Reward tiers mapped to product SKUs
   - Fulfilment plan and timeline for backers
   - Stretch goals that are actually achievable
4. **If investor funding:**
   - Materials needed (deck, financials, prototype)
   - Outreach timeline
   - Term sheet expectations
   - What to have ready for due diligence
5. **If supplier payment terms:**
   - What terms to negotiate (deposit %, milestone payments, net terms)
   - How to build supplier confidence for better terms
6. **Contingency** — what if funding falls short? What's the minimum viable production run?
7. **Cash flow bridge** — the gap between money out (production) and money in (first sales). How long is it and how is it covered?
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
Production development is complete. Here are the key outputs:

[FROM ./WORKBOOK.md, every sub-task output and its footer — read it, or paste here if you have no file access]

Synthesise into a HANDOVER for Phase 08 (Launch Preparation). Include:
1. Production status and readiness
2. Final landed cost and margin
3. Production timeline and key dates
4. Quality plan summary
5. Compliance/certification status
6. Supply chain risks
7. Inventory and fulfilment readiness
8. Confidence rating
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a QA manager who has to stand behind the first production run. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 08 (Launch Preparation) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Production ready** — Tooling approved, quality plan set, timeline locked. Proceed to launch prep.
- **Production delayed** — Specific issues delaying production. Identify resolution path.
- **Cost problem** — Landed cost exceeds target. Design changes or scope reduction needed.
- **Supplier issue** — Current supplier can't deliver. Need to find alternative.

