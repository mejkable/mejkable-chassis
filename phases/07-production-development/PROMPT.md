# Phase 07 — Production Development: PROMPT

## Agent Context

You are assisting with the Production Development phase. Your role is to help navigate manufacturing decisions, supplier evaluation, quality planning, and production logistics.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../06-prototyping-validation/HANDOVER.md` for frozen design and production inputs
- `./BRIEF.md` for this phase's sub-tasks and done criteria

---

## Sub-Task Prompts

### Supplier Selection & Evaluation

```
I need to evaluate and select manufacturers for this product:

Product: [USER INSERTS DESCRIPTION AND KEY MANUFACTURING REQUIREMENTS]
BOM: [USER INSERTS OR SUMMARISES]
Volume: [USER INSERTS INITIAL AND ANNUAL VOLUME ESTIMATES]
Location preference: [Domestic / Overseas / No preference]
Budget: [USER INSERTS TOOLING AND UNIT COST TARGETS]

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

```
I'm preparing for a DFM (Design for Manufacturing) review with my manufacturer:

Design: [USER INSERTS DESIGN DESCRIPTION, KEY FEATURES, MATERIALS]
Manufacturing process: [USER INSERTS — e.g., injection moulding, PCB assembly, offset print]
Known concerns: [USER INSERTS ANY AREAS THEY'RE UNSURE ABOUT]

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

```
I need a quality plan for manufacturing this product:

Product: [USER INSERTS DESCRIPTION]
Key quality requirements: [USER INSERTS FROM REQUIREMENTS — critical dimensions, visual standards, functional requirements]
Manufacturing process: [USER INSERTS]
Volume: [USER INSERTS]

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

```
Help me build a comprehensive landed cost model:

BOM: [USER INSERTS FINAL BOM WITH UNIT COSTS]
Manufacturing cost: [USER INSERTS QUOTED MANUFACTURING PRICE]
Tooling: [USER INSERTS TOOLING COSTS AND EXPECTED LIFE]
Volume: [USER INSERTS ORDER QUANTITY]

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

```
Help me build a production timeline for:

Product: [USER INSERTS DESCRIPTION]
Target launch date: [USER INSERTS OR "help me determine"]
Key milestones known: [USER INSERTS — e.g., tooling already ordered]

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

```
I need to fund production for this product:

Total capital required:
- Tooling: [USER INSERTS]
- First production run: [USER INSERTS]
- Packaging: [USER INSERTS]
- Certification/testing: [USER INSERTS]
- Freight & logistics: [USER INSERTS]
- Buffer/contingency: [USER INSERTS]
- **Total:** [USER INSERTS]

Funding path chosen: [USER INSERTS — crowdfunding, angel, PO financing, supplier terms, bootstrap, etc.]
Production timeline: [USER INSERTS KEY DATES]
Cash available now: [USER INSERTS]

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

## Synthesis Prompt

```
Production development is complete. Here are the key outputs:

[USER PASTES SUPPLIER INFO, COSTS, TIMELINE, QUALITY PLAN]

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

## Decision Point

- **Production ready** — Tooling approved, quality plan set, timeline locked. Proceed to launch prep.
- **Production delayed** — Specific issues delaying production. Identify resolution path.
- **Cost problem** — Landed cost exceeds target. Design changes or scope reduction needed.
- **Supplier issue** — Current supplier can't deliver. Need to find alternative.

