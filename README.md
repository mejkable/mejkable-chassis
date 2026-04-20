<br>

<p align="center">
  <img src=".github/assets/logo.svg" alt="Mejkable" height="96">
</p>

<p align="center">
  <img src=".github/assets/wordmark.svg" alt="mejkable" height="52">
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/mejkable/mejkable-chassis?style=flat-square" alt="License"></a>
  <img src="https://img.shields.io/github/v/tag/mejkable/mejkable-chassis?label=version&style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/status-alpha-orange?style=flat-square" alt="Status">
  <img src="https://img.shields.io/badge/template-repo-blue?style=flat-square" alt="Template">
</p>

<p align="center">
  <sub><b>Alpha.</b> Phases, sub-tasks and conventions may shift between releases. See <code>CHANGELOG.md</code> and <code>ROADMAP.md</code>.</sub>
</p>

<br>

# Mejkable Chassis

**An agentic product development chassis for physical products.**

A markdown-based framework that guides hardware and manufactured goods from opportunity discovery through post-launch iteration, using AI agents at every stage. Built for solopreneurs, lean teams, and anyone who wants structure without a SaaS.

> No code. No database. No app. Just markdown files that instruct agents, capture work, record decisions, and hand context between phases.

## Why this exists

Most product development frameworks are either rigid gate-based processes built for large companies, or vague "move fast" advice that falls apart when you actually have to ship physical things. Hardware has real constraints: suppliers, tooling, packaging, certification, shipping. AI agents are powerful but stateless, and lose the plot across long projects.

The chassis is the frame that holds the work together. Each of the 10 phases has standardised files that tell an agent what to do, capture what it produces, and pass structured context to the next phase. Your preferred AI harness (Claude Code, Codex, OpenCode, Cursor, Aider) does the thinking, the chassis keeps it coordinated.

## The 10 phases

| # | Phase | Focus |
|---|---|---|
| 00 | Opportunity Discovery | Where's the opportunity? Is it worth pursuing? |
| 01 | Problem Definition | What exactly is the problem and who has it? |
| 02 | Research & Insight | What do we need to know before designing? |
| 03 | Product Definition | What are we building and what are the boundaries? |
| 04 | Concept Development | What could it look like? |
| 05 | Design Development | How exactly is it constructed? |
| 06 | Prototyping & Validation | Does it work and does it meet the need? |
| 07 | Production Development | How do we make it at scale? |
| 08 | Launch Preparation | How do we get it to customers? |
| 09 | Post-Launch & Iteration | What did we learn and what comes next? |

Phases 00, 02, 07, and 08 include funding sub-tasks. Sub-tasks within each phase are a menu, not a fixed checklist. Each project selects what applies.

## How it works

Every phase has the same five files:

- **BRIEF.md** — Phase definition, sub-task menu, done criteria
- **PROMPT.md** — Copy-paste-ready agent prompts for each sub-task
- **WORKBOOK.md** — Where agent outputs and working material land
- **DECISIONS.md** — Every meaningful choice, with rationale
- **HANDOVER.md** — Structured summary passed to the next phase

HANDOVER is the glue between phases. It's what the next phase reads first.

## Quick start

### Option 1: Use this template (recommended)

Click **"Use this template"** at the top of the [GitHub repo](https://github.com/mejkable/mejkable-chassis) to spawn your own project repo with a fresh history.

Then:
```bash
cd my-product
mv library/templates/AGENTS.project-starter.md AGENTS.md
# Fill in PROJECT.md
# Open in your preferred agent harness
# Go to the entry phase's BRIEF.md and start
```

### Option 2: Clone and re-init

```bash
git clone https://github.com/mejkable/mejkable-chassis my-product
cd my-product
rm -rf .git
git init
mv library/templates/AGENTS.project-starter.md AGENTS.md
# Fill in PROJECT.md and commit
```

See `WORKFLOW.md` for the full template-vs-live-project model, including how improvements flow from live projects back to the template.

## Agent harness support

The chassis is harness-agnostic. It uses the `AGENTS.md` convention (supported by Claude Code via a `@AGENTS.md` shim in `CLAUDE.md`, natively by Codex, OpenCode, Cursor, Aider, and others).

Configure which AI service handles which task in `config/PROVIDERS.md`. Prompts in the chassis stay provider-agnostic.

## Recommended tools

The chassis is plain markdown, so any editor works. A few that suit it especially well:

- **[Obsidian](https://obsidian.md)** — free for personal use. Opens the repo as a vault. Graph view and backlinks make the flow between phases and decisions visible. Canvas is useful for the messier early phases.
- **[Typora](https://typora.io)** — paid, WYSIWYG. Excellent for drafting and reading individual phase files when you want the markdown rendered as you type.
- **VS Code** or any editor with a markdown preview pane — works fine, no setup needed.

The chassis uses standard markdown (relative links, no `[[wikilinks]]`) so files render correctly on GitHub and in every editor. Obsidian still derives backlinks from standard links.

## What this is good for

- Physical consumer products (electronics, home goods, personal care, lifestyle)
- Games, content products, printed goods
- Design-led premium products with brand requirements
- Anything with suppliers, tooling, packaging, or certification
- Solo founders and small teams who want coordination without process overhead

## What this is not

- A SaaS or app — it's a folder of markdown files
- A replacement for a CAD tool, ERP, or PLM
- A gate-based enterprise process — the structure is guidance, not bureaucracy
- Prescriptive — every project picks its own path through the sub-task menus

## Contributing

Improvements are welcome. The cleanest way to contribute is:

1. Use the chassis on a real project
2. When you hit friction, note it in your project's `CHASSIS-NOTES.md`
3. Open an issue or PR against this repo with the improvement

See `WORKFLOW.md` for the internal improvement flow.

## License

MIT. See `LICENSE`.

## Credits

Built by [Mejkable](https://mejkable.com).
