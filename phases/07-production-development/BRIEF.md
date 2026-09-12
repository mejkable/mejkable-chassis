# Phase 07 — Production Development: BRIEF

## Purpose

Bridge from validated design to reliable, repeatable manufacturing. This phase answers: **"How do we make this at scale, at cost, at quality — and who makes it?"**

This is where the product leaves the design studio and enters the factory. Tooling is ordered, suppliers are contracted, quality systems are defined, and the supply chain is built. Decisions here lock in cost and quality for the life of the product.

---

## Inputs Needed

- Phase 06 HANDOVER.md — frozen design, final BOM, validated cost estimate, compliance needs
- Phase 02 research — manufacturing methods, supplier landscape, regulatory requirements
- Volume forecasts and budget for tooling/setup

---

## Sub-Task Menu

Sub-tasks are a menu, not a checklist. Which ones this project runs is decided by the Phase Plan prompt in `PROMPT.md` and recorded under Phase Plan in `WORKBOOK.md`, never by ticking boxes here: this file is not edited in a live project. Core sub-tasks carry a short expansion (what it produces, how it is run, when to skip) to help you choose; Conditional and Optional keep the one-line form.

### Core (recommended for all projects)

- [ ] **Supplier selection & contracting** — Evaluate, select, and engage manufacturers. Get quotes, review capabilities, negotiate terms.
  *Produces:* a scored supplier comparison, sent RFQs, returned quotes and a selected supplier with agreed terms. *Run as:* RFQs to 3–5 suppliers using the agent's framework and templates; three to six weeks of calendar time. *Skip when:* a supplier is already contracted from a previous product and has quoted this one.
- [ ] **Design for Manufacturing (DFM) review** — Formal manufacturability review with selected supplier. Identify and resolve production issues before tooling.
  *Produces:* the manufacturer's requested changes, each accepted or rejected against the requirements. *Run as:* with the supplier's engineer, prepared with the DFM Review Preparation prompt; one to two weeks including their turnaround. *Skip when:* never for tooled or assembled products. For simple print work it collapses into press proofing.
- [ ] **Tooling & setup planning** — Define tooling requirements, timelines, and costs. Moulds, dies, print plates, fixtures, jigs.
  *Produces:* the tooling list with cost, lead time and ownership terms. *Run as:* with the selected supplier, captured in the WORKBOOK; a week of exchanges. *Skip when:* the process needs no tooling, such as CNC or digital print.
- [ ] **Quality plan** — Define quality standards, inspection criteria, testing protocols, and acceptable quality levels (AQL).
  *Produces:* incoming, in-process and final inspection criteria, AQL levels, a golden-sample definition and a corrective-action process. *Run as:* solo with the agent, then reviewed by a QC or sourcing specialist; half a day plus review. *Skip when:* the first run is so small you will inspect every unit yourself, and say so.
- [ ] **Production costing** — Final landed cost calculation including manufacturing, tooling amortisation, packaging, shipping, duties, warehousing.
  *Produces:* the landed cost model, margin at target price, break-even volume and sensitivity. *Run as:* solo with the agent over real quotes; two hours once quotes are in. *Skip when:* never. Phase 08 prices from this.
- [ ] **Production timeline** — End-to-end timeline from tooling order through first shipment.
  *Produces:* the end-to-end schedule from tooling order to first shippable unit, with buffers and the critical path. *Run as:* solo with the agent, checked against supplier-confirmed lead times; two hours. *Skip when:* never. Launch timing in Phase 08 depends on it.
- [ ] **Critique** — A fresh session in the sceptical role named in `PROMPT.md` reads the draft HANDOVER against the done criteria and returns gaps, unsupported claims and its own confidence rating. Run last, before the handover is marked final.
  *Produces:* a list of gaps against the done criteria, claims to downgrade to Estimated or Unknown, and a second confidence rating. *Run as:* a separate session with only the draft HANDOVER and this BRIEF; 30 minutes, then an hour to act on it. *Skip when:* never. Disagreements between producer and critic go in DECISIONS.md.

### Conditional (select based on product type)

- [ ] **Pre-production sample approval** — Define the sample approval process. What samples are needed before mass production begins?
- [ ] **Certification & compliance execution** — Submit for formal testing and certification. Manage the process, respond to findings.
- [ ] **Packaging production** — Separate production stream for packaging: print proofing, structural samples, production.
- [ ] **Assembly planning** — If assembly is separate from component manufacturing: define assembly process, location, labour, QC.
- [ ] **Electronics manufacturing planning** — PCB production, SMT assembly, firmware flashing, functional testing, programming jigs.
- [ ] **Print production planning** — For printed products: press proofing, colour matching, paper sourcing, print run planning, finishing (lamination, varnish, die-cut).
- [ ] **Logistics & fulfilment setup** — Warehousing, pick-and-pack, shipping carriers, customs/import documentation.
- [ ] **Inventory planning** — Initial order quantities, reorder triggers, safety stock, lead time management.
- [ ] **Production funding execution** — If external funding is needed for tooling and first production run: execute the funding plan from Phase 00/02. This may mean launching a crowdfunding campaign, closing an investment round, applying for purchase order financing, or negotiating supplier payment terms. Align funding timeline with production timeline.

### Optional / Deep Dive

- [ ] **Second source identification** — Backup suppliers for critical components or processes.
- [ ] **Production FMEA** — Failure mode analysis for the production process itself. What could go wrong in manufacturing?
- [ ] **Sustainability in production** — Waste reduction, energy use, ethical manufacturing verification.
- [ ] **Landed cost modelling** — Detailed model including duties, tariffs, freight, currency risk for international sourcing.
- [ ] **Scale-up planning** — What changes when volumes increase 5x or 10x? Plan ahead.

---

## Done Criteria

1. Manufacturer(s) selected and contracted
2. DFM review completed and all issues resolved
3. Tooling ordered or ready to order
4. Quality plan defined and agreed with manufacturer
5. Final production cost is known and margin is acceptable
6. Compliance/certification path is on track
7. Production timeline is established with key milestones
8. The Critique has been run in a fresh session and its findings addressed, or the disagreement recorded in DECISIONS.md
9. HANDOVER provides everything needed to begin launch preparation in parallel

---

## Notes

- This phase often overlaps with Phase 08 (Launch Preparation). Marketing and sales planning can begin as soon as the product and timeline are sufficiently defined. Don't wait until production is complete to start launch work.
- For first-time hardware makers: budget more time and money for this phase than you think. Tooling delays, DFM changes, and sample iterations are normal.
- Quality planning is not optional. Define what "good" looks like before production starts, not after you receive a shipment.
- Get everything in writing with suppliers: specifications, timelines, payment terms, quality standards, IP protection, defect handling.

