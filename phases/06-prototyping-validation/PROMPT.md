# Phase 06 — Prototyping & Validation: PROMPT

## Agent Context

You are assisting with the Prototyping & Validation phase. Your role is to help plan tests, structure user feedback, analyse results, and guide design iteration decisions.

Before beginning, read:
- `../../PROJECT.md` for project identity and constraints
- `../05-design-development/HANDOVER.md` for the design and prototype plan
- `../03-product-definition/HANDOVER.md` for requirements to test against
- `./BRIEF.md` for this phase's purpose, sub-task menu and done criteria
- `./WORKBOOK.md` § Phase Plan for the approved sub-task list, once the Phase Plan prompt below has been run

Work under the Operating Policy in `../../AGENTS.md`: tag every figure, standard, supplier or competitor **Verified**, **Estimated** or **Unknown** and never invent a citation; ask before changing a recorded decision, marking a phase `complete` or committing money; run only the sub-task selected.

---

## How to Use This Prompt

Each sub-task below is a standalone prompt. Run them individually, capture outputs in WORKBOOK.md, and use the synthesis prompt at the end to pull everything together for the HANDOVER.

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
- `../05-design-development/HANDOVER.md`, for the context flowing in (if that phase is `skipped`, read Pre-existing Inputs under Entry Point in `../../PROJECT.md` instead)
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

### Prototype Build Planning

```
I'm ready to build prototypes for this product:

Design: [USER INSERTS DESIGN SUMMARY AND KEY SPECS]
Prototype roadmap: [USER INSERTS FROM PHASE 05]
Budget: [USER INSERTS AVAILABLE BUDGET]
Timeline: [USER INSERTS TARGET TIMELINE]

Help me create a detailed prototype build plan:

1. **Prototype 1: [Type]**
   - Exact specification (what's being made, to what fidelity)
   - Build method and vendor/source
   - Materials and components needed
   - Timeline: order date → delivery → ready for testing
   - Cost estimate
   - What this prototype will and won't tell us

2. [Repeat for each prototype in the roadmap]

3. **Parallel activities** — what can happen while prototypes are being built?
4. **Risk mitigation** — what if a prototype fails or is delayed?
5. **Total budget and timeline summary**
```

### User Testing Plan

```
I need to plan user testing for this product:

Product: [USER INSERTS DESCRIPTION]
Target user: [USER INSERTS FROM PHASE 01]
Prototype available: [USER DESCRIBES WHAT THE PROTOTYPE IS AND ITS FIDELITY]
Key questions to answer: [USER INSERTS — from prototype roadmap]

Help me create a user testing plan:

1. **Participants** — how many, what profile, how to recruit
2. **Test format** — in-person vs. remote, moderated vs. unmoderated, individual vs. group
3. **Test protocol** — step-by-step guide for the test session:
   - Introduction and context setting
   - Tasks to perform or scenarios to experience
   - Observation points (what to watch for)
   - Questions to ask (open-ended, specific)
   - Rating scales if useful
4. **What NOT to do** — common testing mistakes to avoid (leading questions, explaining too much)
5. **Success metrics** — how will we know if the test results are positive?
6. **Documentation plan** — how to capture observations and feedback during sessions
7. **Analysis framework** — how to synthesise findings across participants
```

### Test Results Analysis

```
I've completed prototype testing. Here are the raw results:

[USER PASTES TEST DATA, OBSERVATIONS, USER FEEDBACK]

Help me analyse:

1. **Summary of findings** — what did we learn?
2. **Requirements validation** — which requirements are confirmed met, which are not?
3. **User feedback themes** — what patterns emerge from user testing?
4. **Critical issues** — problems that must be fixed before production
5. **Improvement opportunities** — things that could be better but aren't blockers
6. **Surprises** — anything unexpected (positive or negative)?
7. **Design change recommendations** — specific changes, prioritised by impact and effort
8. **Re-test needs** — what needs to be tested again after changes?
```

### Design Iteration Tracking

```
Based on prototype testing, these design changes are proposed:

[USER INSERTS PROPOSED CHANGES]

Help me evaluate and track each change:

| Change | Reason | Impact on Requirements | Cost Impact | Risk | Priority | Decision |
|---|---|---|---|---|---|---|
| | | | | | | Approve/Reject/Defer |

For approved changes:
- What needs to be modified (design files, BOM, specs)?
- Does this require a new prototype, or can it be validated analytically?
- Timeline impact?
- Who needs to be informed (suppliers, partners)?
```

### Design Freeze Checklist

```
We're preparing to freeze the design for production. Current state:

[USER INSERTS CURRENT DESIGN STATUS AND ANY OUTSTANDING ITEMS]

Run through a design freeze checklist:

1. **All Must-Have requirements met?** — yes/no with evidence
2. **User testing completed and findings addressed?**
3. **All critical issues from testing resolved?**
4. **BOM finalised?** — all parts, materials, sources confirmed
5. **Design files complete and current?** — CAD, artwork, die-lines all reflecting latest changes
6. **Packaging design finalised?**
7. **Regulatory compliance path clear?** — required testing identified, timeline known
8. **Cost estimate current?** — reflects final design, not earlier versions
9. **Outstanding risks documented and accepted?**
10. **Stakeholder sign-off?** — everyone who needs to approve has approved

List any items that are NOT yet resolved and the plan to close them.
```

---

## Output Capture

Capture each sub-task's output in WORKBOOK.md under a heading matching the sub-task name. Every output ends with the Sub-Task Output Footer defined in `config/CONVENTIONS.md`: **Sources & confidence**, **Assumptions made**, **Open questions**, **Candidate decisions**. Keep the four headings even when one is empty; the Critique prompt checks them and the synthesis prompt reads from them.

---

## Synthesis Prompt

```
Prototyping and validation is complete. Here are the key results:

[USER PASTES TEST RESULTS, ITERATION HISTORY, FREEZE CHECKLIST STATUS]

Synthesise into a HANDOVER for Phase 07 (Production Development). Include:
1. Validation summary — what was tested and confirmed
2. Final design status
3. Outstanding items from design freeze checklist
4. Key learnings that affect production
5. Risk areas for manufacturing
6. Confidence rating
```

---

## Critique Prompt

Run this in a **fresh session**, not the one that produced the work. The critic reads the draft handover and the done criteria, nothing else the producer wrote unless it asks. Record disagreements between producer and critic in DECISIONS.md rather than resolving them silently.

```
You are a test and validation engineer who has seen prototypes pass tests that did not matter. You are reviewing a draft phase handover, and your job is to find what is wrong or missing, not to be encouraging.

Read:
- `./HANDOVER.md`, the draft handover for this phase
- `./BRIEF.md` § Done Criteria, what this phase was supposed to deliver
- `./WORKBOOK.md`, only where you need to check a claim against its source

Return:
1. **Gaps against the done criteria** — which criteria are not met, or met only on paper
2. **Unsupported claims** — every figure, standard, supplier, competitor or user statement in the handover that is not tagged Verified with a source you can follow. Say which should be downgraded to Estimated or Unknown.
3. **Assumptions treated as facts** — where the handover has quietly converted an assumption into a constraint
4. **What Phase 07 (Production Development) will trip over** — the three things most likely to cause rework downstream if left as they are
5. **Your confidence rating** for this handover: High / Medium / Low, with one sentence on what drives it. Where it differs from the producer's rating, say why.

Be specific. Quote the line you are challenging. Do not rewrite the handover; that is the producer's job.
```

---

## Decision Point

- **Design frozen** — Validated and ready for production development. Proceed.
- **Another iteration needed** — Specific issues require another prototype round. Iterate within this phase.
- **Fundamental issue discovered** — Testing reveals a problem that requires returning to Phase 04 or 05.
- **User rejection** — Testing shows users don't want this. Return to Phase 01 or 03 to reassess.

