# library/templates/

Files that are copied or moved into place rather than used where they sit.

## In the chassis (template repo)

- `AGENTS.project-starter.md` becomes the root `AGENTS.md` of a live project at scaffold time
- `README.project-starter.md` becomes the root `README.md` of a live project at scaffold time

Both are moved out by the scaffold steps in `WORKFLOW.md`, "Setting Up a New Live Project". After scaffolding, this folder holds only this file (delete `README.project-starter.md` if you chose not to use it).

## In a live project

Use this folder for the project's own reusable blanks: a supplier RFQ letter, a user-interview guide, a test protocol sheet, a packaging spec form. Name them kebab-case with a `-template` suffix (`supplier-rfq-template.md`, `interview-guide-template.md`) so a filled-in copy elsewhere is never mistaken for the blank.

If a template turns out to be useful beyond this project, note it in `CHASSIS-NOTES.md` so it can be considered for the chassis.
