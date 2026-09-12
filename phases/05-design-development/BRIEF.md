# Phase 05 — Design Development: BRIEF

## Purpose

Turn the selected concept into a fully resolved, buildable design. This phase answers: **"How exactly is this product constructed, and is it ready to prototype?"**

This is where concept becomes engineering. CAD models, detailed drawings, material specifications, component selection, and assembly planning all happen here. The output should be detailed enough to build a representative prototype.

---

## Inputs Needed

- Phase 04 HANDOVER.md — selected concept, design parameters, visual direction
- Phase 03 HANDOVER.md — requirements, target specifications, constraints
- Phase 02 research on materials, manufacturing, and regulations for reference

---

## Sub-Task Menu

Sub-tasks are a menu, not a checklist. Which ones this project runs is decided by the Phase Plan prompt in `PROMPT.md` and recorded under Phase Plan in `WORKBOOK.md`, never by ticking boxes here: this file is not edited in a live project. Core sub-tasks carry a short expansion (what it produces, how it is run, when to skip) to help you choose; Conditional and Optional keep the one-line form.

### Core (recommended for all projects)

- [ ] **Detailed design development** — Resolve the concept into a complete design. All parts, dimensions, interfaces, and assembly defined. For physical products this typically means CAD. For print products this means production-ready artwork layout.
  *Produces:* the resolved design: all parts, dimensions and interfaces, as CAD or production artwork. *Run as:* outside the chassis in design tools, by you or a contracted designer; days to weeks depending on complexity. *Skip when:* never. The WORKBOOK holds decisions and file references, not the files.
- [ ] **Material specification** — Final material selections for all components. Specific grades, suppliers, colours, finishes.
  *Produces:* a per-component material selection with grade, supplier candidates, cost impact and rationale. *Run as:* solo with the agent, then confirmed with a materials supplier or engineer; half a day plus supplier replies. *Skip when:* materials were fixed by the concept and confirmed in Phase 04.
- [ ] **Assembly & construction planning** — How does it go together? Assembly sequence, fastening methods, tolerances, fit requirements.
  *Produces:* the BOM, assembly sequence, fastening methods and critical interfaces. *Run as:* solo with the agent, reviewed by someone who has assembled similar products; half a day. *Skip when:* the product is a single part or a printed item with no assembly.
- [ ] **Design review against requirements** — Systematic check: does the design meet every Must-Have requirement from Phase 03? Document compliance or deviations.
  *Produces:* a requirement-by-requirement compliance table with blockers and trade-offs flagged. *Run as:* solo with the agent once the design is near-final; two hours. *Skip when:* never. Unmet Must-Haves found here are cheap; in Phase 07 they are not.
- [ ] **Prototyping strategy** — What prototypes are needed, in what order, and what does each one test? Define the prototype roadmap for Phase 06.
  *Produces:* the prototype roadmap: which prototypes, what each answers, method, cost, sequence. *Run as:* solo with the agent, reviewed by whoever builds the prototypes; two hours. *Skip when:* Phase 06 is being skipped entirely, which needs a DECISIONS.md entry.
- [ ] **Critique** — A fresh session in the sceptical role named in `PROMPT.md` reads the draft HANDOVER against the done criteria and returns gaps, unsupported claims and its own confidence rating. Run last, before the handover is marked final.
  *Produces:* a list of gaps against the done criteria, claims to downgrade to Estimated or Unknown, and a second confidence rating. *Run as:* a separate session with only the draft HANDOVER and this BRIEF; 30 minutes, then an hour to act on it. *Skip when:* never. Disagreements between producer and critic go in DECISIONS.md.

### Conditional (select based on product type)

- [ ] **CAD modelling** — 3D CAD development for moulded, machined, or fabricated parts. Define what software and file formats are needed downstream.
- [ ] **PCB & electronics design** — Schematic design, PCB layout, component placement, connector specification. Firmware requirements definition.
- [ ] **Print production design** — Card layout, print sheet imposition, die-line design, colour specification (Pantone/CMYK), paper/card stock specification.
- [ ] **Graphic design production** — Final artwork, illustration, typography, icon design. Production-ready files in required formats.
- [ ] **Structural packaging design** — Die-lines, material specification, insert design, assembly method, print specification for packaging.
- [ ] **Engineering analysis** — Stress analysis, thermal analysis, drop test simulation, battery life modelling — whatever analysis validates the design before prototyping.
- [ ] **DFM pre-check** — Early design-for-manufacturing review. Share designs with potential manufacturers for feedback before finalising.
- [ ] **Finish & CMF specification** — Colour, Material, Finish specification document. Surface textures, coatings, plating, printing methods.
- [ ] **User interface design** — If the product has a UI: button layout, display design, LED patterns, sound design, mode logic.

### Optional / Deep Dive

- [ ] **Tolerance analysis** — Critical tolerance stack-ups and their impact on assembly and function.
- [ ] **Cost engineering** — Detailed COGS estimate based on actual design. Part-by-part costing.
- [ ] **Sustainability assessment** — Environmental impact of material and manufacturing choices. Recyclability analysis.
- [ ] **Design FMEA** — Failure mode and effects analysis at the design level. What could go wrong and how severe are the consequences?

---

## Done Criteria

1. Design is fully resolved — all parts, materials, and interfaces are defined
2. Design meets all Must-Have requirements (deviations documented and accepted)
3. Files are in a format suitable for prototyping
4. A clear prototyping strategy exists for Phase 06
5. Manufacturing feasibility has been sanity-checked
6. HANDOVER.md provides everything needed to begin prototyping

---

## Notes

- This phase often involves external tools and partners: CAD software, graphic design tools, freelance designers, engineering consultants. The chassis captures decisions and outputs, not the entire design workflow.
- "Fully resolved" doesn't mean "perfect." It means detailed enough to prototype and learn. Some details will be refined after prototype testing in Phase 06.
- For products with both physical and graphic design components (a game with illustrated cards, a product with branded packaging, a kit with printed materials), these workstreams may run in parallel. Track them separately in the WORKBOOK.
- Design files themselves (CAD, artwork, etc.) live in the library/assets folder or in external tools. WORKBOOK captures decisions, specifications, and references to those files.

