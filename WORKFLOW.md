# WORKFLOW.md — Managing the Chassis and Live Projects

## The Three Repos

You will maintain three (or more) separate git repos:

```
~/projects/
├── mejkable-chassis/             ← THE TEMPLATE (the "master" chassis)
├── my-product-a/                 ← LIVE PROJECT (scaffolded from template)
└── my-product-b/                 ← LIVE PROJECT (scaffolded from template)
```

Each has a different purpose and different rules about what gets edited.

---

## What Lives Where

### Template Repo (`mejkable-chassis/`)

This is the **blank, reusable chassis**. It contains:

- AGENTS.md and CLAUDE.md (harness instructions, kept generic — no project-specific content)
- PROJECT.md (blank template)
- config/ (CONVENTIONS.md, PROVIDERS.md as templates)
- All phase folders with BRIEF.md, PROMPT.md, WORKBOOK.md, DECISIONS.md, HANDOVER.md
- library/ (empty, with placeholder structure)
- journal/LOG.md (blank template)
- This file (WORKFLOW.md)

**Rules:**
- BRIEF.md and PROMPT.md files get improved here based on learnings from live projects
- WORKBOOK.md, DECISIONS.md, HANDOVER.md stay as blank templates
- Never put project-specific content in this repo
- Tag releases: `v0.1`, `v0.2`, etc. when you make meaningful improvements

### Live Project Repos (`my-product-a/`, `my-product-b/`)

These are **working copies** where real project work happens. They contain:

- Everything from the template, PLUS
- Filled-in PROJECT.md with project-specific identity and vision
- Filled-in config/PROVIDERS.md with actual provider choices
- Phase files filled with real work: WORKBOOK entries, DECISIONS logged, HANDOVER written
- library/ populated with actual research, assets, and reference materials
- journal/LOG.md with real project events

**Rules:**
- WORKBOOK.md, DECISIONS.md, HANDOVER.md are actively edited with project content
- BRIEF.md and PROMPT.md should NOT be edited here (see "Improvement Flow" below)
- AGENTS.md can be extended with project-specific context at the bottom (CLAUDE.md is a thin shim that imports AGENTS.md)

---

## Setting Up a New Live Project

```bash
# 1. Copy the template (or use GitHub's "Use this template" button)
cp -r mejkable-chassis/ my-product/
cd my-product/

# 2. Swap in the live-project AGENTS.md
mv library/templates/AGENTS.project-starter.md AGENTS.md
# CLAUDE.md stays as-is (it's a thin shim that imports AGENTS.md)

# 3. Initialise a fresh repo (if you used cp, not "Use this template")
rm -rf .git
git init

# 4. Record which template version this was created from
echo "Created from mejkable-chassis v0.1" >> CHANGELOG.md
git add .
git commit -m "init: scaffold from mejkable-chassis v0.1"

# 5. Fill in PROJECT.md
# 6. Start working
```

---

## The Daily Workflow

### Working on a live project

```
1. Open the project repo in your preferred agent harness (Claude Code, Codex, OpenCode, Cursor, Aider, etc.)
2. The agent reads AGENTS.md automatically → knows the system
3. Check PROJECT.md → see current phase and status
4. Go to current phase folder
5. Read BRIEF.md → understand the phase and select sub-tasks
6. Use PROMPT.md → copy relevant sub-task prompts, run them
7. Paste outputs into WORKBOOK.md
8. Log decisions in DECISIONS.md
9. When phase is complete → write HANDOVER.md
10. Update PROJECT.md status tracker
11. Commit: "phase-02: complete competitive deep-dive"
```

### Noticing a chassis improvement while working

This is the critical moment. You're working on a live project and you realise:
- A sub-task is missing from the BRIEF
- A prompt could be better worded
- The HANDOVER template needs an extra field
- A new sub-task category is needed

What you do depends on the type of change:

**Prompt improvements (most common):**
You don't need to change any files to test this. You're already copying prompts from PROMPT.md and pasting them into agent sessions. So try the improved wording immediately in your current session. If the output is better, note it in CHASSIS-NOTES.md and keep working. Apply it to the template repo later.

The live project's WORKBOOK captures whatever the agent produced — it doesn't matter which version of the prompt generated it.

**Structural changes (new sub-task, new handover field, new file):**
These require file changes. Use a branch in the live project:

```bash
# In the live project repo:
git checkout -b test/new-handover-field

# Make the structural change
# Work with it for the current phase
# If it works:
git checkout main
git merge test/new-handover-field
# Then apply the same change to the template repo

# If it doesn't work:
git checkout main
git branch -D test/new-handover-field
# Note what went wrong in CHASSIS-NOTES.md
```

**Changes to completed phases:**
Don't backport. The phase worked well enough to produce a handover. Improving the template for future projects is sufficient. Retrofitting finished work isn't worth the effort.

---

## The Improvement Flow

There are two paths depending on urgency:

### Fast path (try it now, apply to template later)

```
Working in live project
        │
        ├── Prompt improvement?
        │   → Try new wording directly in agent session
        │   → Output goes in WORKBOOK as normal
        │   → Note improvement in CHASSIS-NOTES.md
        │   → Apply to template repo later
        │
        └── Structural change?
            → Branch in live project
            → Apply change on branch
            → Work with it for the current phase
            → If it works: merge branch, note in CHASSIS-NOTES.md, apply to template
            → If it doesn't: abandon branch, note what failed
```

### Slow path (batch improvements to template)

```
┌─────────────────────┐
│  Live Project 1     │──── discovers improvement ────┐
│                     │                               │
└─────────────────────┘                               ▼
                                              ┌──────────────┐
                                              │ CHASSIS-NOTES │
                                              │ .md (in each  │
                                              │ project repo) │
                                              └──────┬───────┘
┌─────────────────────┐                              │
│  Live Project 2     │──── discovers improvement ───┘
│                     │                               
└─────────────────────┘                               
                                                      │
                                          (periodic review)
                                                      │
                                                      ▼
                                              ┌──────────────┐
                                              │   TEMPLATE    │
                                              │   REPO        │
                                              │ (master       │
                                              │  chassis)     │
                                              └──────┬───────┘
                                                     │
                                              (new version)
                                                     │
                                    ┌────────────────┼────────────────┐
                                    ▼                                 ▼
                          ┌─────────────────┐              ┌─────────────────┐
                          │ Future Project  │              │ Optionally back- │
                          │ (starts fresh   │              │ port to active   │
                          │  from new       │              │ projects if the  │
                          │  template)      │              │ change matters   │
                          └─────────────────┘              └─────────────────┘
```

---

## Testing Template Changes Against Live Projects

The core tension: you can't validate a template improvement without running it against real project content, but you don't want to pollute the live project with experimental changes.

### By change type:

**Prompt changes → test without touching files**
Prompts are copy-pasted into agent sessions anyway. Try the new wording in your next session. The WORKBOOK captures the output. If it's better, the template gets updated. The live project files never changed.

**Sub-task additions → test on a branch**
Branch in the live project, add the sub-task to BRIEF.md, run it, evaluate. Merge if it adds value, discard if it doesn't. Either way, the template gets the learning.

**Handover format changes → test on a branch, only for upcoming phases**
If you're about to write a Phase 03 handover and you think the template needs an extra field, branch, add the field, write the handover with it, and evaluate whether the next phase benefits. Merge or discard.

**Whole new files or major structural changes → test in a scratch copy**
For big changes, copy the live project to a temporary directory and experiment there. This keeps both the live project and the template clean while you figure out if the change works.

```bash
# For major experimental changes:
cp -r my-product-a/ my-product-a-scratch/
cd my-product-a-scratch/
# Make structural changes, test them, evaluate
# If they work → apply to template repo, then backport to live project
# Delete the scratch copy when done
rm -rf my-product-a-scratch/
```

---

## Backporting Template Improvements to Live Projects

After improvements are tested and applied to the template, you may want to pull them into active projects.

**When to backport:**
- A new sub-task is added that's relevant to a phase you haven't started yet
- A prompt is significantly improved for a phase you're about to enter
- A structural change to HANDOVER format that you want going forward

**When NOT to backport:**
- The phase is already complete in the live project (the old format worked fine)
- The change is minor wording improvement
- You're mid-phase and switching formats would create inconsistency

**How to backport (manual, selective):**

```bash
# From the live project directory, selectively copy specific files:
cp ../mejkable-chassis/phases/05-design-development/BRIEF.md ./phases/05-design-development/BRIEF.md
cp ../mejkable-chassis/phases/05-design-development/PROMPT.md ./phases/05-design-development/PROMPT.md

git add .
git commit -m "backport: updated phase-05 BRIEF and PROMPT from chassis v0.2"
```

Only backport BRIEF.md and PROMPT.md — never overwrite WORKBOOK.md, DECISIONS.md, or HANDOVER.md in a live project.

---

## CHASSIS-NOTES.md Format

Keep this in the root of each live project repo:

```markdown
# Chassis Improvement Notes

Notes captured during live project work. To be reviewed and applied to the
template repo periodically.

## [Date] — [Phase where discovered]

**File:** [e.g., phases/02-research-insight/BRIEF.md]
**Type:** [Missing sub-task / Prompt improvement / Template gap / Structural change]
**Description:** [What should change and why]
**Priority:** [High — needed for next project / Medium — would be nice / Low — minor polish]

---
```

---

## Git Workflow Summary

### Template repo

```
main branch only (or main + dev if you prefer)
Tag releases: v0.1, v0.2, v1.0
Commit messages: "add funding sub-tasks to phases 00,02,07,08"
```

### Live project repos

```
main branch for the primary development path
Branches for exploratory work within a phase (optional)
Tags for phase completions: phase-00-complete, phase-01-complete
Commit messages: "phase-02: complete competitive deep-dive"
                  "phase-02: decision — proceed to product definition"
                  "backport: updated phase-05 from chassis v0.2"
```

---

## Recommended Review Cadence

| Activity | When | Where |
|---|---|---|
| Commit project work | After each sub-task or decision | Live project repo |
| Note chassis improvements | As they're discovered | CHASSIS-NOTES.md in live project |
| Review and apply improvements | Weekly, or between phases | Template repo |
| Tag template version | After a batch of improvements | Template repo |
| Backport to live projects | Only when entering a new phase | Live project repo |
| Full chassis retrospective | After a project completes | Template repo |

---

## After a Project Completes

When a project reaches Phase 09 or is otherwise finished, do a full retrospective on the chassis:

1. Review CHASSIS-NOTES.md for any un-applied improvements
2. Review each phase's WORKBOOK and DECISIONS for friction points
3. Ask: which sub-tasks were never used? Which were missing?
4. Ask: which prompts produced great output? Which needed heavy editing?
5. Ask: did the handover format carry the right information between phases?
6. Apply all learnings to the template repo
7. Tag a new template version
8. Archive the completed project repo (it's a record of the full development journey)

---

## Multi-Project Parallel Work

If running multiple live projects simultaneously:

- Each is its own repo, its own context
- When switching between projects, just point your agent at the other project directory — AGENTS.md gives the agent the context automatically
- Chassis improvements may come from either project — both feed into the same template repo
- Don't cross-pollinate project-specific content between live projects (they're independent)
- DO cross-pollinate structural learnings (via the template repo)
