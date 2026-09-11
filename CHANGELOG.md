# Changelog — Mejkable Chassis

## v0.2 — (unreleased)

- Add an Operating Policy section (data integrity tags, ask-vs-proceed, scope discipline) to `library/templates/AGENTS.project-starter.md`
- Add append-only and revisiting rules as Non-Negotiables 8–10 in `library/templates/AGENTS.project-starter.md` and a matching section in `config/CONVENTIONS.md`
- Add a Phase Progression Patterns section (parallel in-progress, revisit loop, skipped) to `config/CONVENTIONS.md`; soften Non-Negotiable 2 in `library/templates/AGENTS.project-starter.md` to "before closing a phase, even an interim one"; add pointers in `AGENTS.md` and `WORKFLOW.md`
- Trim `AGENTS.md` to point at `config/CONVENTIONS.md` and `WORKFLOW.md` instead of restating status values, confidence ratings and formats; drop the duplicated decision-log field list from `library/templates/AGENTS.project-starter.md`
- Add a Closing a session step to `library/templates/AGENTS.project-starter.md` (update Running Notes, append to `journal/LOG.md`, commit); add a not-yet-initialised marker and a one-screen rule to `PROJECT.md`

## v0.1 — Initial Public Release (2026-04-17)

- 10 phases fully built out (00 through 09)
- 5 core files per phase: BRIEF, PROMPT, WORKBOOK, DECISIONS, HANDOVER
- Harness-agnostic agent instructions via AGENTS.md (with CLAUDE.md shim for Claude Code)
- Config: PROVIDERS.md, CONVENTIONS.md
- Funding sub-tasks included in phases 00, 02, 07, 08
- WORKFLOW.md covers template-vs-live-project flow

### Phases included:
- 00 — Opportunity Discovery
- 01 — Problem Definition
- 02 — Research & Insight
- 03 — Product Definition
- 04 — Concept Development
- 05 — Design Development
- 06 — Prototyping & Validation
- 07 — Production Development
- 08 — Launch Preparation
- 09 — Post-Launch & Iteration
