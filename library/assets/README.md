# library/assets/

Visual and binary material: sketches, renders, mood boards, CAD exports, photos of prototypes, packaging dielines, logos, brand files. Markdown files reference these by path; they never embed them (Non-Negotiable 6 in `AGENTS.md`).

## Structure

One folder per asset type at the top level, kebab-case:

```
library/assets/
├── sketches/
├── renders/
├── cad/
├── photos/
├── brand/
└── packaging/
```

Add types as needed. If a folder grows past a few dozen files, split by phase or by concept underneath it.

## File naming

Descriptive, lowercase, hyphenated, per the Naming Conventions in `config/CONVENTIONS.md`. Lead with the subject, end with a two-digit sequence number so versions sort: `concept-a-side-view-01.png`, `enclosure-rev-b-exploded-02.step`. Prefix with the phase number when the asset belongs to one phase's work and nowhere else: `04-concept-a-side-view-01.png`.

Dated captures (prototype photos, test footage) take a `YYMMDD-` prefix like dated research does.

## Large files

CAD, layered image files and video get big fast. Either track them with git-lfs or keep them in external storage and commit a small `.md` next to where the file would be, holding the link and a one-line description. `.gitignore` has commented-out patterns for the common large formats; uncomment what you use.

## Linking from phase work

Reference assets from `WORKBOOK.md` and `HANDOVER.md` by relative path, e.g. `../../library/assets/renders/04-concept-a-side-view-01.png`. Superseded assets stay in place; bump the sequence number rather than overwriting, so a decision that cites version 01 still points at what was actually looked at.
