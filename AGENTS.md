# AGENTS.md, Mejkable Chassis (Template)

## What This Is

This is **the template repo** for Mejkable Chassis, a markdown-based product development framework for hardware and physical products. It provides the structure (phases, file roles, prompts, conventions) that gets copied into live project repos.

No project-specific work happens here. Live projects are scaffolded from this template and evolve independently. Improvements discovered in live projects flow back via `CHASSIS-NOTES.md` entries in each project, then get applied here.

See `WORKFLOW.md` for the full improvement flow (live project, CHASSIS-NOTES.md, template repo, future projects).

## Agent Harness Note

This file is `AGENTS.md`, which Claude Code, Codex, OpenCode, Cursor, Aider, and other harnesses read automatically. A thin `CLAUDE.md` shim sits alongside it for Claude Code compatibility, importing this file via `@AGENTS.md`.

## Repo Role Rules

**This repo (template):**
- Edit `BRIEF.md` and `PROMPT.md` files to improve them across all future projects
- Keep `WORKBOOK.md`, `DECISIONS.md`, `HANDOVER.md` as blank templates
- Never add project-specific content
- Tag releases (`v0.1`, `v0.2`) when improvements are meaningful

**Live project repos (scaffolded from this template):**
- Their root `AGENTS.md` comes from `library/templates/AGENTS.project-starter.md`, not from this file
- Fill `WORKBOOK`, `DECISIONS`, `HANDOVER` per phase
- Never edit `BRIEF` or `PROMPT`, note improvements in each project's `CHASSIS-NOTES.md`

## Repo Structure

```
mejkable-chassis/
├── AGENTS.md                              ← You are here (maintainer-facing)
├── CLAUDE.md                              ← Thin shim, imports AGENTS.md
├── README.md                              ← Public-facing overview
├── LICENSE                                ← MIT
├── PROJECT.md                             ← Blank template for live projects
├── WORKFLOW.md                            ← Template vs live project management
├── CHANGELOG.md                           ← Template version history
├── config/
│   ├── PROVIDERS.md
│   └── CONVENTIONS.md
├── phases/
│   └── NN-phase-name/                     ← BRIEF, PROMPT, WORKBOOK, DECISIONS, HANDOVER
├── library/
│   ├── research/
│   ├── assets/
│   └── templates/
│       └── AGENTS.project-starter.md      ← Becomes AGENTS.md in a live project
└── journal/
    └── LOG.md
```

Phases 00, 02, 07, and 08 include funding-related sub-tasks.

## Sub-Task Flexibility

Sub-tasks within each phase are a menu, not a checklist. Each project selects what applies based on category and entry point. `BRIEF.md` files contain the menu.

## Key Conventions (canonical home: `config/CONVENTIONS.md`)

- **Phase status values:** `not-started`, `in-progress`, `complete`, `skipped`, `revisiting`
- **Confidence ratings:** High / Medium / Low (Low is useful signal, not failure)
- **Decision log format:** date, options considered, chosen, rationale, downstream impact, decider
- **Handover format:** see `phases/*/HANDOVER.md` headings

## Scaffolding a New Live Project

See `WORKFLOW.md`, "Setting Up a New Live Project". Key step after copying: swap `library/templates/AGENTS.project-starter.md` in as the root `AGENTS.md`. The `CLAUDE.md` shim stays unchanged.

## Don't Do in This Repo

- Don't add project-specific content to any file
- Don't edit `library/templates/AGENTS.project-starter.md` without considering whether this file should change too
- Don't ship a chassis improvement without bumping `CHANGELOG.md` and tagging a new version
