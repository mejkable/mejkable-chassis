# AGENTS.md

This file provides guidance to AI agents (Claude Code, Codex, OpenCode, Cursor, Aider, etc.) when working in this repository.

## What This Repo Is

This is a live project scaffolded from [Mejkable Chassis](https://mejkable.com), a markdown-based framework that guides physical products from opportunity discovery through post-launch iteration across 10 phases.

There is no code, no build step, no tests. The `.md` files ARE the system. They instruct agents, capture work, record decisions, and hand context between phases.

`WORKFLOW.md` covers the template-vs-live-project distinction and backport rules. Only needed when you notice a chassis improvement and want to propose it back upstream.

## Project Identity

<!-- Fill in after scaffolding, then delete this comment. -->

- **Name:**
- **Category:**
- **One-line description:**
- **Scaffolded from:** mejkable-chassis vX.Y on YYYY-MM-DD

See `PROJECT.md` for full identity, vision, constraints, and the phase status tracker.

## How to Work Here

### Starting or resuming a session
1. Read `PROJECT.md` for current phase and status
2. Go to the current phase folder
3. Read the previous phase's `HANDOVER.md` (the context flowing in)
4. Read the current phase's `BRIEF.md` and select sub-tasks from the menu
5. Execute sub-tasks using `PROMPT.md`, capture output in `WORKBOOK.md`
6. Log every meaningful choice in `DECISIONS.md` (format in `config/CONVENTIONS.md`)
7. On phase completion, write `HANDOVER.md`, update `PROJECT.md`, commit

### Closing a session
Do this at the end of every working session, not only at phase completion:
1. Update Running Notes in `PROJECT.md` with anything the next session must know to pick up where you stopped (open threads, waiting-on items, a decision that is half-made)
2. Append a dated entry to `journal/LOG.md`
3. Commit

`PROJECT.md` stays under one screen. It is the map, not the record: `WORKBOOK.md` is the file that grows, and `journal/LOG.md` holds the history. When Running Notes fill up, move the detail into the current phase's `WORKBOOK.md` and keep only the pointer.

### Single sources of truth
- `config/CONVENTIONS.md`, file roles, decision format, handover format, status values, naming, confidence ratings
- `config/PROVIDERS.md`, which AI service handles which task type (prompts themselves stay provider-agnostic)

## Operating Policy

1. **Data integrity.** Every number, standard, supplier, competitor or citation you produce is tagged **Verified** (source given), **Estimated** (method given) or **Unknown**. Never invent a standard reference, a price point, a tariff rate, a market figure or a source. If you cannot find it, say so and mark it Unknown; an honest gap is worth more than a plausible fill.
2. **Ask before, proceed on.** Ask the user before changing a recorded decision, marking a phase `complete`, or committing money (orders, deposits, tooling, subscriptions). Proceed without asking on drafting, research and synthesis.
3. **Scope.** Run only the sub-task selected. Do not widen it, pull in neighbouring sub-tasks, or edit files outside the current phase. If something out of scope needs doing, note it in `WORKBOOK.md` and raise it, then stop.

## Non-Negotiables

1. **Never edit `BRIEF.md` or `PROMPT.md` in this repo.** If they need improvement, note it in `CHASSIS-NOTES.md` for later backport to the template. Editing them here breaks the template's improvement flow.
2. **Always write `HANDOVER.md` before closing a phase, even an interim one.** It is the interface between phases, skipping it breaks downstream context. Phases may overlap or loop; the patterns for that (parallel in-progress, revisit, skipped) are in `config/CONVENTIONS.md` under Phase Progression Patterns.
3. **Every meaningful choice goes in `DECISIONS.md` with rationale.** Future-you needs to know WHY, not just WHAT.
4. **Every phase has a gate decision** (go, no-go, pivot, return). Record it in `DECISIONS.md` before advancing `PROJECT.md`.
5. **External work counts too.** CAD sessions, supplier calls, workshop findings. Capture outcomes in the relevant `WORKBOOK.md` or `DECISIONS.md`. The chassis is a coordination tool, not a cage.
6. **Don't put binary or design files in markdown.** Reference their location in `library/assets/` instead.
7. **Don't treat confidence ratings as pass/fail.** "Low" is useful signal, not failure.
8. **`DECISIONS.md` and `journal/LOG.md` are append-only.** Supersede a past entry with a new one that references it. Never edit or delete what is already there.
9. **A `complete` phase's `HANDOVER.md` is only touched after its status is set to `revisiting`** in `PROJECT.md` and the reason is logged in that phase's `DECISIONS.md`.
10. **Never change another phase's files while working in the current one.** If a finding affects an earlier or later phase, note it in the current `WORKBOOK.md` and raise it with the user.

## Git Workflow

- Commit after each sub-task or decision
- Commit messages reference the phase, e.g. `phase-02: complete competitive deep-dive`, `phase-03: decision, premium tier positioning`
- Tag phase completions, e.g. `phase-00-complete`, `phase-01-complete`
- Branch for exploratory alternatives within a phase (optional)
