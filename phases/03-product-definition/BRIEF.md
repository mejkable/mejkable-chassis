# Phase 03 — Product Definition: BRIEF

## Purpose

Translate research and problem understanding into a concrete product specification. This phase answers: **"What are we building, what must it do, and what are the boundaries?"**

This is the bridge between understanding and creation. The output is a product definition document that concept development and design can work against. It's not a final spec — it's a target to aim at.

---

## Inputs Needed

- Phase 02 HANDOVER.md — market position, feasibility boundaries, regulatory requirements, pricing framework
- Phase 01 HANDOVER.md — problem statement, user profile, priority jobs-to-be-done
- Any pre-existing design briefs, brand guidelines, or stakeholder requirements

---

## Sub-Task Menu

Sub-tasks are a menu, not a checklist. Which ones this project runs is decided by the Phase Plan prompt in `PROMPT.md` and recorded under Phase Plan in `WORKBOOK.md`, never by ticking boxes here: this file is not edited in a live project. Core sub-tasks carry a short expansion (what it produces, how it is run, when to skip) to help you choose; Conditional and Optional keep the one-line form.

### Core (recommended for all projects)

- [ ] **Requirements definition** — Functional requirements (what it must do), performance requirements (how well), and constraints (what it must not do or exceed).
  *Produces:* functional, performance and constraint requirements, each with source, priority and a way to verify it. *Run as:* solo with the agent from the Phase 01 and 02 handovers, then reviewed with whoever will design or make the product; half a day plus review. *Skip when:* never.
- [ ] **User experience definition** — How the user interacts with the product from discovery through disposal. Key moments, touchpoints, and experience goals.
  *Produces:* a journey from discovery to end of life, with the ideal experience, friction points and design implications at each stage. *Run as:* a short workshop if you have a team, otherwise solo with the agent; two to three hours. *Skip when:* the product is a component or B2B part with no consumer experience to design.
- [ ] **Target specification** — Measurable targets: dimensions, weight, battery life, material properties, player count, component count — whatever is quantifiable for this product.
  *Produces:* a table of measurable targets with acceptable ranges and competitor benchmarks. *Run as:* solo with the agent, then checked with an engineer or manufacturer for the technical rows; half a day, longer if you measure competitor units. *Skip when:* the requirements are already fully quantified.
- [ ] **Prioritisation framework** — Must-have vs. should-have vs. nice-to-have. Use MoSCoW or similar to rank requirements. This is where trade-offs begin.
  *Produces:* a MoSCoW ranking with the contested calls and the minimum lovable product marked out. *Run as:* a workshop with everyone who has a say; two hours. *Skip when:* a single decision-maker has already ranked the requirements in DECISIONS.md.
- [ ] **Success criteria** — How will you know the product is good enough? Define measurable benchmarks for launch readiness.
  *Produces:* the measurable benchmarks that say the product is good enough to launch. *Run as:* solo with the agent from the requirements and targets; an hour. *Skip when:* never. Phase 06 tests against these.
- [ ] **Critique** — A fresh session in the sceptical role named in `PROMPT.md` reads the draft HANDOVER against the done criteria and returns gaps, unsupported claims and its own confidence rating. Run last, before the handover is marked final.
  *Produces:* a list of gaps against the done criteria, claims to downgrade to Estimated or Unknown, and a second confidence rating. *Run as:* a separate session with only the draft HANDOVER and this BRIEF; 30 minutes, then an hour to act on it. *Skip when:* never. Disagreements between producer and critic go in DECISIONS.md.

### Conditional (select based on product type)

- [ ] **Brand & identity requirements** — Visual language, brand values, design principles that the product must express. (Critical for design-heavy products)
- [ ] **Packaging requirements** — Functional needs (protection, retail display, shipping), brand expression, unboxing experience, regulatory labelling.
- [ ] **Content & IP definition** — For products with content (games, books, educational products): scope, quantity, quality standards, IP considerations.
- [ ] **Electronic/technical specification** — For products with electronics: component spec, power requirements, connectivity, firmware scope, LED specifications, charging requirements.
- [ ] **SKU & variant strategy** — Will there be multiple versions, sizes, colours, editions? Define the initial SKU plan.
- [ ] **Accessory & ecosystem definition** — Are there add-ons, refills, expansions, or companion products? Define the product boundary.
- [ ] **Sustainability requirements** — Material restrictions, recyclability targets, packaging waste goals, certifications to pursue.

### Optional / Deep Dive

- [ ] **Benchmark teardown synthesis** — If competitor teardowns were done in Phase 02, translate findings into specification targets. "At least as good as X in durability, better than Y in weight."
- [ ] **Risk-driven requirements** — Requirements that exist specifically to mitigate risks identified in earlier phases.
- [ ] **Cost target breakdown** — Allocate the target COGS across major sub-assemblies or components. This constrains concept development productively.

---

## Done Criteria

1. A clear, prioritised requirements document exists
2. Target specifications are quantified where possible
3. Trade-off priorities are explicit (what gives when something has to give)
4. Success criteria are defined and measurable
5. The definition is specific enough to generate concepts against, but not so prescriptive that it dictates solutions
6. The Critique has been run in a fresh session and its findings addressed, or the disagreement recorded in DECISIONS.md
7. HANDOVER.md provides a complete brief for concept development

---

## Notes

- The art of product definition is being specific enough to be useful and loose enough to allow creativity. "The product must weigh less than 200g" is good. "The product must use aluminium" is usually too prescriptive at this stage (unless driven by a validated requirement).
- Requirements should be traceable — each one should connect back to a user need, market insight, or technical constraint from previous phases.
- For products with existing design direction (where core gameplay, artwork, or form comes as near-finished input), this phase is about defining everything AROUND the given input — manufacturing spec, packaging, component quality, etc.

