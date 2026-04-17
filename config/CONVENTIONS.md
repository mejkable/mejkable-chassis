# CONVENTIONS.md — Standards & Practices

## File Roles

Every phase folder contains the same core files:

| File | Role | Who writes it |
|---|---|---|
| **BRIEF.md** | Defines the phase — purpose, inputs needed, sub-tasks, done-criteria | Chassis (template) + user customisation |
| **PROMPT.md** | Agent instructions — provider-agnostic task framing for AI-assisted work | Chassis (template) + user customisation |
| **WORKBOOK.md** | Working output — findings, drafts, iterations, raw material | Agent + user |
| **DECISIONS.md** | Choices made, options considered, rationale, owner | User (agent can draft) |
| **HANDOVER.md** | Structured summary passed to the next phase | Agent + user review |

---

## Phase Status Values

| Status | Meaning |
|---|---|
| `not-started` | Phase has not begun |
| `in-progress` | Actively being worked |
| `complete` | Done-criteria met, handover written |
| `skipped` | Intentionally bypassed — record reason in DECISIONS.md |
| `revisiting` | Returning to this phase based on later findings |

---

## Confidence Rating

Each phase handover includes a confidence rating:

| Rating | Meaning |
|---|---|
| **High** | Work is thorough, decisions are well-supported, low risk moving forward |
| **Medium** | Core work done but gaps remain — acceptable to proceed with awareness |
| **Low** | Significant unknowns — proceeding carries risk, consider revisiting |

Include a brief note on what would raise confidence if it's Medium or Low.

---

## Sub-Task Flexibility

Sub-tasks within each phase are **not fixed**. They depend on:

- Product category (electronics vs. printed goods vs. furniture vs. textiles)
- Project entry point (what's already done)
- Specific choices made in earlier phases

Each BRIEF.md contains a **core sub-task menu** — a list of possible sub-tasks for that phase. The user selects or adds to these based on their project. This is the primary flexibility mechanism.

---

## Decision Log Format

Decisions in DECISIONS.md follow this structure:

```
### [Decision Title]
- **Date:** [Date]
- **Options considered:** [List]
- **Chosen:** [Which option]
- **Rationale:** [Why]
- **Impact on:** [Which downstream phases or constraints this affects]
- **Decided by:** [Who — user, agent recommendation accepted, etc.]
```

---

## Handover Format

Every HANDOVER.md follows this structure:

```
## Phase [Number] — [Name] Handover

### Summary
[2-3 sentence overview of what was accomplished]

### Confidence: [High / Medium / Low]
[Brief note on what drives the rating and what would raise it]

### Key Findings
[Bulleted list of the most important outputs]

### Decisions Made
[Reference key decisions from DECISIONS.md]

### Open Questions
[What remains unresolved and needs attention downstream]

### Constraints Established
[Any new boundaries, requirements, or non-negotiables identified]

### Inputs for Next Phase
[Specific items the next phase needs to pick up]
```

---

## Naming Conventions

- Folders: lowercase, hyphenated, prefixed with phase number (`00-opportunity-discovery`)
- Core files: UPPERCASE.md (`BRIEF.md`, `PROMPT.md`, etc.)
- Supporting files: lowercase, hyphenated (`market-sizing-notes.md`, `competitor-matrix.md`)
- Assets: descriptive, lowercase, hyphenated (`led-candle-concept-sketch-01.png`)

---

## Working Outside the Chassis

Development work often happens outside this system — in CAD software, on a workbench, in conversations with suppliers, in a factory. That's expected and good.

When external work produces decisions or findings relevant to the project:
1. Capture the outcome in the relevant phase's WORKBOOK.md or DECISIONS.md
2. Update the HANDOVER.md if the phase summary changes
3. Note it in the project LOG.md

The chassis is a thinking and coordination tool, not a cage.

