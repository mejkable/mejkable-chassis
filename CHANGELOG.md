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
- Define the fixed Sub-Task Output Footer (Sources & confidence, Assumptions made, Open questions, Candidate decisions) in `config/CONVENTIONS.md`
- Replace the freeform retrospective questions in `WORKFLOW.md` with a fixed per-phase scorecard (used, output quality 1–3, prompt edited, handover sufficient); add the same table as an optional block in `CHASSIS-NOTES.md`
- Wrap the placeholder note entry in `CHASSIS-NOTES.md` in an HTML comment labelled as a template, so a skim no longer reads it as content
- Align cross-file wording: `config/CONVENTIONS.md` file-roles table no longer says BRIEF and PROMPT take user customisation in a live project; the `WORKFLOW.md` CHASSIS-NOTES format block matches the shipped `CHASSIS-NOTES.md`; session-close step added to the Daily Workflow in `WORKFLOW.md`; starter session steps and single-sources list in `library/templates/AGENTS.project-starter.md` match the softened handover rule and the new CONVENTIONS sections
- Echo a one-line Operating Policy pointer (Verified / Estimated / Unknown tags, ask-vs-proceed, scope) in the Agent Context of every `phases/**/PROMPT.md`
- Add a Before you run a sub-task block (list unclear points, ask one question if material, otherwise state assumptions and proceed) under How to Use This Prompt in every `phases/**/PROMPT.md`, adding that section where it was missing
- Add an Output Capture section to every `phases/**/PROMPT.md` pointing at the Sub-Task Output Footer in `config/CONVENTIONS.md`
- Add a Phase Plan prompt at the top of every `phases/**/PROMPT.md` (agent proposes sub-tasks from the BRIEF menu, user approves, agreed list goes under Phase Plan in WORKBOOK.md); Agent Context read lists now point at that section; session step 4 in `library/templates/AGENTS.project-starter.md` and Daily Workflow step 5 in `WORKFLOW.md` follow suit
- Add a Critique prompt to every `phases/**/PROMPT.md`: a fresh session in a named sceptical role per phase (investor, user researcher, product manager, design director, DFM engineer, validation engineer, QA manager, launch lead, head of operations) reviews the draft handover against the done criteria and returns gaps, unsupported claims and its own confidence rating

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
