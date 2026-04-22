# Roadmap

Proposed changes for upcoming versions of the chassis. Items move from here to `CHANGELOG.md` once applied and released. Each version bucket gets a review session where every entry is assessed for impact and necessity before anything is applied.

**Entry states:**
- `proposed` — captured, not yet reviewed
- `approved` — passed review, ready to apply
- `deferred` — pushed to a later version
- `rejected` — decided against, kept here briefly then pruned

**Workflow:**
1. Friction surfaces (from a live project, from chassis use, or direct insight). Add a `proposed` entry to the next-version section below.
2. Run a review session. Walk through every `proposed` item, decide approve / defer / reject.
3. Cut a release branch (`release/v0.X`) off `main` before applying anything. All v0.X changes land on this branch.
4. Apply approved items to the chassis on the release branch. Add lines to `CHANGELOG.md` as each item ships.
5. When the bucket is done, merge `release/v0.X` into `main`, tag the new version on `main`, and remove shipped entries from this file.

---

## v0.2

### Scaffold step for CLAUDE.md customisation
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** `WORKFLOW.md`'s "Setting Up a New Live Project" section says "Fill in PROJECT.md" and stops. `CLAUDE.md` also needs live-project tailoring (project identity line, removal of any template-only hints, optional entry-phase hint), but the scaffold flow does not call that out. Result: freshly scaffolded projects ship with a generic `CLAUDE.md`.
- **Impact:** Add an explicit scaffold step, "Tailor CLAUDE.md: set project identity line, remove template-only sections." Also revisit `library/templates/AGENTS.project-starter.md` to ensure it is clearly a starter and not a duplicate of the chassis AGENTS.md.
- **Priority:** High
- **Status:** proposed
- **Affected files:** `WORKFLOW.md`, `library/templates/AGENTS.project-starter.md`

### Scaffold handling of README.md and LICENSE
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17 (backport note)
- **Date:** 2026-04-19
- **Motivation:** When scaffolding a live project from the chassis, the chassis's `README.md` (framework overview) and `LICENSE` (MIT for the chassis itself) get copied across. The README is misleading in a live project, it describes the framework rather than the product. The LICENSE covers the chassis scaffold, not the project's own content which may have different terms.
- **Impact:** Update the scaffold flow to explicitly say "delete or replace `README.md`" and "replace `LICENSE` with the project's own licence, or remove it if undecided." Optionally ship a minimal `README.project-starter.md` in `library/templates/` that points at `PROJECT.md`.
- **Priority:** High
- **Status:** proposed
- **Affected files:** `WORKFLOW.md`, `library/templates/AGENTS.project-starter.md`, possibly new `library/templates/README.project-starter.md`

### Guidance on parallel and looping phases
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** The chassis defines `revisiting` as a phase status but never explains when or how to use it. Non-Negotiable #2 ("Always write `HANDOVER.md` before advancing to the next phase") reads strictly linear, which collides with real hardware work where phases overlap constantly (e.g. Phase 02 research tails run alongside Phase 03 product definition). Without explicit guidance, users either follow the rule rigidly and block on external dependencies, or abandon handover discipline and lose context.
- **Impact:** Add a "Phase Progression Patterns" section to `config/CONVENTIONS.md` covering three patterns, (1) parallel in-progress with interim HANDOVER at Low confidence, (2) revisit loop via the `revisiting` status, (3) `skipped` phases logged in `DECISIONS.md`. Soften Non-Negotiable #2 to "Always write `HANDOVER.md` before *closing* a phase, even an interim one" and cross-reference the patterns.
- **Priority:** High
- **Status:** proposed
- **Affected files:** `config/CONVENTIONS.md`, `AGENTS.md`, `library/templates/AGENTS.project-starter.md`, `WORKFLOW.md`

### AGENTS.md drift against CONVENTIONS.md
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** Originally flagged in Candela as CLAUDE.md duplicating content from `config/CONVENTIONS.md` and `WORKFLOW.md` (repo tree, file-roles table, phase status values, confidence ratings). CLAUDE.md became a thin `@AGENTS.md` shim in v0.1, but AGENTS.md still mirrors those canonical values. Same drift risk, different file.
- **Impact:** Trim AGENTS.md so it references `config/CONVENTIONS.md` and `WORKFLOW.md` rather than duplicating their values. Keep AGENTS.md focused on agent-harness behaviour, repo role rules, and pointers.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `AGENTS.md`, `library/templates/AGENTS.project-starter.md`
- **Note:** Verify the scope of remaining duplication during review, v0.1 already resolved part of the original concern.

### Fresh-scaffold marker in PROJECT.md
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** A freshly scaffolded live project is visually indistinguishable from one mid-work, the only signal is unfilled square-bracket placeholders in tables. Future Claude instances waste cycles verifying whether the repo is initialised.
- **Impact:** Add an explicit top-of-file marker to `PROJECT.md` such as `> Status: not-yet-initialised, fill in the sections below before starting phase work.` User deletes the marker once identity is populated.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `PROJECT.md`

### library/ naming convention and structure guide
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** The chassis ships empty `library/research/`, `library/assets/`, `library/templates/` folders with no guidance on how to organise material. Candela had to derive a convention (topic folder at top level, `YYMMDD Source Topic` for dated inputs, kebab-case for evergreen references, link-back pattern from WORKBOOKs). Every live project re-deriving this is waste.
- **Impact:** Ship `library/research/README.md` in the template with the pre-written convention. Consider matching READMEs for `library/assets/` and `library/templates/`.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** New `library/research/README.md`, possibly new `library/assets/README.md` and `library/templates/README.md`

### Entry-phase guidance for non-Phase-00 projects
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** Candela enters at Phase 03 or 04, not 00. `PROJECT.md`'s Entry Point section asks for "Phase number" and "Reason" with no guidance on how to decide, or what pre-existing inputs each entry phase expects. Users default to 00 without thinking.
- **Impact:** Add a short decision aid to the Entry Point section (or a table by category: design-led vs. problem-led vs. opportunity-led) so the user picks correctly. Consider an "expected prior inputs" checklist per entry phase.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `PROJECT.md`, `library/templates/AGENTS.project-starter.md`

### Major-backport recipe for existing live projects
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17 (backport note)
- **Date:** 2026-04-19
- **Motivation:** `WORKFLOW.md`'s backport section covers selectively copying `BRIEF`/`PROMPT`, but not whole-chassis version jumps (e.g. v0.1-prerelease to v0.1-public) where structural changes land: CLAUDE.md becoming a shim, new AGENTS.md, new `library/templates/AGENTS.project-starter.md`, refreshed `WORKFLOW.md` and `PROVIDERS.md`. A "major backport" checklist would save reinventing the safe set of overwrites vs. preserves every time.
- **Impact:** Add a "Major backport" subsection to `WORKFLOW.md` with explicit preserves (`PROJECT.md`, `CHASSIS-NOTES.md`, completed phase folders, `library/research/**`, `journal/LOG.md` if populated, `config/PROVIDERS.md` if customised) and a list of safe overwrites.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `WORKFLOW.md`

### Sub-task working-format signal in PROMPT.md
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-18
- **Date:** 2026-04-19
- **Motivation:** Several sub-tasks are classically done in teams, workshops, or with external tooling (user interviews, customer research, supplier calls, design critiques), not as a solo founder chatting to an agent. A solo-agent first pass is often good enough for compressed phases, but the chassis should be explicit about when a real team, workshop, or primary-research pass would materially upgrade the output.
- **Impact:** Add a "Best format" line and "Solo fallback quality" line at the top of each sub-task in `PROMPT.md`. Format options: Solo with agent / Workshop (2–6 people) / Primary research (N interviews) / Solo with expert review / External tool (e.g. Dovetail, Miro). Quality: High / Medium / Low with a short note on what gets lost.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `phases/**/PROMPT.md` (all 10 phases, ~30–40 sub-tasks total)

### Progressive disclosure in BRIEF sub-task menus
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-18
- **Date:** 2026-04-19
- **Motivation:** The `BRIEF.md` sub-task menu is a single line per item, enough to recognise a familiar technique but not enough to choose between adjacent items or predict what running one will feel like. The full `PROMPT.md` is one layer away and written as an execution instrument, not a selection aid.
- **Impact:** Per sub-task in `BRIEF.md`, add a two-to-four-sentence expansion covering what it produces, how it is typically run, rough duration, and when to skip. Consider markdown `<details>` blocks to keep the menu scannable.
- **Priority:** Medium
- **Status:** proposed
- **Affected files:** `phases/**/BRIEF.md` (all 10 phases)
- **Note:** Composes naturally with the "working-format signal" entry above, address together to avoid double-touching each BRIEF/PROMPT pair.

### Backport CHASSIS-NOTES placeholder wrap to template
- **Source:** `candela/CHASSIS-NOTES.md` entry dated 2026-04-17
- **Date:** 2026-04-19
- **Motivation:** The chassis template's `CHASSIS-NOTES.md` has a placeholder entry using the same `### [Date]` heading structure as a real note, so a skim treats it as content. The fix (wrap in HTML comment, label "Template for new entries, copy the block below:") was applied in Candela's own file but has not been backported to the chassis template.
- **Impact:** Small mechanical edit to the scaffold template, five-minute change.
- **Priority:** Low
- **Status:** proposed
- **Affected files:** Chassis-side `CHASSIS-NOTES.md` template (verify location during review, likely under `library/templates/` or at repo root)

### Obsidian-friendly link pass
- **Source:** direct (deferred from v0.1 polish)
- **Date:** 2026-04-18
- **Motivation:** Chassis is plain markdown with no cross-links. Obsidian works but does not shine. README recommends Obsidian/Typora, yet the file structure does not take advantage of their features.
- **Impact:** Adds relative standard-markdown links and YAML frontmatter across ~15 files. Non-breaking on GitHub or other editors. Roughly 30 minutes of work.
- **Priority:** Low (polish, not structural)
- **Status:** proposed
- **Affected files:** `PROJECT.md`, `phases/**/BRIEF.md`, `phases/**/HANDOVER.md`, `AGENTS.md`, `WORKFLOW.md`, `CHASSIS-NOTES.md` (template)
- **Scope:**
  1. `PROJECT.md` status table, link each phase name to `phases/NN-name/BRIEF.md`
  2. Each phase's `BRIEF.md`, add "Input from: [previous HANDOVER](../NN-prev/HANDOVER.md)" at the top
  3. Each phase's `HANDOVER.md`, add "Feeds into: [next BRIEF](../NN-next/BRIEF.md)" at the top
  4. `AGENTS.md`, link to `config/CONVENTIONS.md`, `WORKFLOW.md`, each phase folder
  5. `WORKFLOW.md`, convert referenced paths into actual links
  6. `CHASSIS-NOTES.md`, link to the improvement-flow section in `WORKFLOW.md`
  7. YAML frontmatter on `PROJECT.md` and each phase's `BRIEF.md` with `phase`, `status`, `updated` fields
- **Constraint:** Do not use `[[wikilinks]]`, they render literally on GitHub.

---

## v0.3

(no items yet)
