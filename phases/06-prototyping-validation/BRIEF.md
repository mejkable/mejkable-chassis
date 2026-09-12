# Phase 06 — Prototyping & Validation: BRIEF

## Purpose

Build and test prototypes to validate the design before committing to production. This phase answers: **"Does the design actually work, and do users want it?"**

This is where the product meets reality. Prototypes expose problems that analysis missed. User testing reveals whether the product delivers on the jobs-to-be-done. The goal is to de-risk the transition to production.

---

## Inputs Needed

- Phase 05 HANDOVER.md — design files, BOM, prototyping roadmap, test criteria
- Phase 03 requirements — for testing against
- Phase 01 user profile — for user testing recruitment and context

---

## Sub-Task Menu

Sub-tasks are a menu, not a checklist. Which ones this project runs is decided by the Phase Plan prompt in `PROMPT.md` and recorded under Phase Plan in `WORKBOOK.md`, never by ticking boxes here: this file is not edited in a live project. Core sub-tasks carry a short expansion (what it produces, how it is run, when to skip) to help you choose; Conditional and Optional keep the one-line form.

### Core (recommended for all projects)

- [ ] **Prototype build planning** — Finalise prototype specifications, vendor/method selection, timeline, and budget. Execute the roadmap from Phase 05.
  *Produces:* a build plan per prototype with spec, vendor, timeline and cost. *Run as:* solo with the agent from the Phase 05 roadmap; two hours plus quotes. *Skip when:* the prototypes are trivial to make in-house and the roadmap already says how.
- [ ] **Functional validation** — Does the product work as designed? Test against functional and performance requirements.
  *Produces:* pass/fail results per functional and performance requirement. *Run as:* outside the chassis, on the bench or with a test partner, then logged in the WORKBOOK; days. *Skip when:* never for anything that must work. For purely aesthetic products, fold it into the appearance review.
- [ ] **User testing** — Put prototypes in front of target users. Observe, gather feedback, identify problems and opportunities.
  *Produces:* observed reactions, task success and feedback themes from real users with a prototype in hand. *Run as:* moderated sessions with 5–8 participants, planned with the User Testing Plan prompt; a week of calendar time. *Skip when:* the product's use is identical to a proven predecessor, and record that reasoning.
- [ ] **Design iteration** — Based on prototype learnings, refine the design. Track changes and rationale.
  *Produces:* a tracked list of changes with reason, impact and decision. *Run as:* solo with the agent after each test round; an hour per round. *Skip when:* no test failed. Never skip if one did.
- [ ] **Final design freeze** — Lock the design for production. Document what's final and what has tolerance for adjustment.
  *Produces:* the completed freeze checklist and a list of anything still open with a plan to close it. *Run as:* a sign-off meeting with everyone who must approve; an hour. *Skip when:* never. Phase 07 spends money on the frozen design.
- [ ] **Critique** — A fresh session in the sceptical role named in `PROMPT.md` reads the draft HANDOVER against the done criteria and returns gaps, unsupported claims and its own confidence rating. Run last, before the handover is marked final.
  *Produces:* a list of gaps against the done criteria, claims to downgrade to Estimated or Unknown, and a second confidence rating. *Run as:* a separate session with only the draft HANDOVER and this BRIEF; 30 minutes, then an hour to act on it. *Skip when:* never. Disagreements between producer and critic go in DECISIONS.md.

### Conditional (select based on product type)

- [ ] **Appearance prototype review** — Evaluate visual design, CMF, proportions, shelf presence in physical form.
- [ ] **Durability & stress testing** — Drop tests, wear simulation, environmental testing (heat, cold, moisture), repeated use cycles.
- [ ] **Electronics testing** — Functional test of PCB, battery life validation, charging test, LED performance, EMC pre-scan.
- [ ] **Print & production sample review** — For printed products: colour proofing, paper/card stock feel, print quality, die-cutting accuracy.
- [ ] **Gameplay/usability testing** — For interactive products: is it fun? Intuitive? Balanced? Does it create the intended experience?
- [ ] **Packaging prototype testing** — Does packaging protect the product? Does it display well? Is unboxing experience right?
- [ ] **Safety & compliance pre-testing** — Pre-compliance testing before formal certification. Identify issues early.
- [ ] **Shelf & retail simulation** — How does the product look on a shelf? Next to competitors? In different lighting?

### Optional / Deep Dive

- [ ] **Blind comparison testing** — Test your product against competitors with users who don't know which is yours.
- [ ] **Photography & content testing** — Photograph prototypes for early marketing validation. Does it photograph well?
- [ ] **Cost validation** — With physical prototypes in hand, re-validate cost estimates. Any surprises?
- [ ] **Supplier feedback round** — Share prototypes with potential manufacturers for production feedback.

---

## Done Criteria

1. Prototypes have been built and tested against key requirements
2. User testing has been conducted and findings documented
3. Critical design issues have been resolved through iteration
4. Design is frozen and documented for production handover
5. Remaining risks are identified and accepted or mitigated
6. HANDOVER provides a production-ready design package

---

## Notes

- Prototype iterations are normal and expected. Budget for at least 2-3 rounds. The cost of iteration here is tiny compared to the cost of fixing problems after tooling.
- User testing doesn't need to be formal. 5-8 people from the target audience using the prototype and sharing honest feedback is enormously valuable.
- "Design freeze" doesn't mean nothing can ever change. It means the design is stable enough to begin production planning. Minor refinements may still happen in Phase 07.
- For solopreneurs: this phase can be the most time-consuming and expensive pre-production phase. Plan accordingly.

