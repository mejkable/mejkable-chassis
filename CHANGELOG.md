# Changelog — Mejkable Chassis

## v0.2 — (unreleased)

- Add an Operating Policy section (data integrity tags, ask-vs-proceed, scope discipline) to `library/templates/AGENTS.project-starter.md`
- Add append-only and revisiting rules as Non-Negotiables 8–10 in `library/templates/AGENTS.project-starter.md` and a matching section in `config/CONVENTIONS.md`
- Add a Phase Progression Patterns section (parallel in-progress, revisit loop, skipped) to `config/CONVENTIONS.md`; soften Non-Negotiable 2 in `library/templates/AGENTS.project-starter.md` to "before closing a phase, even an interim one"; add pointers in `AGENTS.md` and `WORKFLOW.md`
- Trim `AGENTS.md` to point at `config/CONVENTIONS.md` and `WORKFLOW.md` instead of restating status values, confidence ratings and formats; drop the duplicated decision-log field list from `library/templates/AGENTS.project-starter.md`
- Add a Closing a session step to `library/templates/AGENTS.project-starter.md` (update Running Notes, append to `journal/LOG.md`, commit); add a not-yet-initialised marker and a one-screen rule to `PROJECT.md`
- Add an entry-phase decision aid (rule of thumb plus table by starting point with expected prior inputs) to the Entry Point section of `PROJECT.md`; point the session-start steps in `library/templates/AGENTS.project-starter.md` at Pre-existing Inputs when earlier phases are skipped
- Add a scaffold step to `WORKFLOW.md` for filling Project Identity in `AGENTS.md` and deleting the placeholder comment; reword that comment in `library/templates/AGENTS.project-starter.md` to point at the scaffold checklist
- Add scaffold steps to `WORKFLOW.md` for replacing `README.md` and `LICENSE`; ship a minimal `library/templates/README.project-starter.md` that points at `PROJECT.md`; note the check in the starter's scaffold comment in `library/templates/AGENTS.project-starter.md`
- Add `library/research/README.md`, `library/assets/README.md` and `library/templates/README.md` with the folder structure, naming and link-back conventions, replacing the `.gitkeep` files; list them in the `AGENTS.md` repo tree and point at them from Naming Conventions in `config/CONVENTIONS.md`
- Add a Major backport subsection to `WORKFLOW.md` with explicit preserve, safe-to-overwrite and merge-by-hand lists for whole-chassis version jumps

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
