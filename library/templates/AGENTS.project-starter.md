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
6. Log every meaningful choice in `DECISIONS.md` (date, options, chosen, rationale, impact, decider)
7. On phase completion, write `HANDOVER.md`, update `PROJECT.md`, commit

### Single sources of truth
- `config/CONVENTIONS.md`, file roles, decision format, handover format, status values, naming, confidence ratings
- `config/PROVIDERS.md`, which AI service handles which task type (prompts themselves stay provider-agnostic)

## Non-Negotiables

1. **Never edit `BRIEF.md` or `PROMPT.md` in this repo.** If they need improvement, note it in `CHASSIS-NOTES.md` for later backport to the template. Editing them here breaks the template's improvement flow.
2. **Always write `HANDOVER.md` before advancing to the next phase.** It is the interface between phases, skipping it breaks downstream context.
3. **Every meaningful choice goes in `DECISIONS.md` with rationale.** Future-you needs to know WHY, not just WHAT.
4. **Every phase has a gate decision** (go, no-go, pivot, return). Record it in `DECISIONS.md` before advancing `PROJECT.md`.
5. **External work counts too.** CAD sessions, supplier calls, workshop findings. Capture outcomes in the relevant `WORKBOOK.md` or `DECISIONS.md`. The chassis is a coordination tool, not a cage.
6. **Don't put binary or design files in markdown.** Reference their location in `library/assets/` instead.
7. **Don't treat confidence ratings as pass/fail.** "Low" is useful signal, not failure.

## Git Workflow

- Commit after each sub-task or decision
- Commit messages reference the phase, e.g. `phase-02: complete competitive deep-dive`, `phase-03: decision, premium tier positioning`
- Tag phase completions, e.g. `phase-00-complete`, `phase-01-complete`
- Branch for exploratory alternatives within a phase (optional)
