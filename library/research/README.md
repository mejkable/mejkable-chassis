# library/research/

Raw inputs and reference material that phase work draws on: reports, articles, interview notes, standards summaries, supplier documents, competitor teardowns. Nothing here is a project output; outputs live in the phase `WORKBOOK.md` files.

## Structure

One folder per topic at the top level, named in kebab-case. Topics follow the subject, not the phase, because the same material is read across several phases.

```
library/research/
├── market/
├── users/
├── competitors/
├── materials-and-processes/
├── regulatory/
└── suppliers/
```

Add or rename topics as the project needs. Do not nest deeper than two levels.

## File naming

Follow the Naming Conventions in `config/CONVENTIONS.md`: lowercase, hyphenated, no spaces.

- **Dated inputs** (a report, an interview, a supplier quote, a snapshot of a competitor's pricing) are prefixed with the date so they sort chronologically and their age is visible at a glance: `YYMMDD-source-topic.md`, e.g. `260315-interview-p04-storage-habits.md`, `260402-trade-press-category-overview.md`
- **Evergreen references** (a standards summary, a glossary, a materials comparison you keep updating) carry no date: `plastics-comparison.md`, `ce-marking-summary.md`
- Non-markdown originals (PDFs, spreadsheets, exports) sit next to the note that summarises them, same stem, original extension

## Linking from phase work

Every `WORKBOOK.md` entry that uses research links back to the file it drew on by relative path, e.g. `../../library/research/users/260315-interview-p04-storage-habits.md`. The link is what lets a later phase, or the Critique sub-task, check a claim against its source. Untraceable research is treated as **Estimated** at best under the Operating Policy in `AGENTS.md`.

When a research file is superseded, keep the old one and add a line at the top pointing at the replacement. Do not delete inputs; they explain why past decisions looked right at the time.
