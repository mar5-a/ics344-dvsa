# ICS344 DVSA Project

This repository is organized for a report-first workflow.

Use the Word/Google Docs report as the polished deliverable, and use this repo to store:

- code and configuration changes
- raw screenshots and logs
- exact commands used
- lesson-by-lesson notes
- supporting scripts

## Suggested workflow

1. Reproduce one lesson.
2. Save raw evidence under `evidence/lesson-XX-*`.
3. Apply the fix and save code/config notes under that lesson folder and `fixes/` if needed.
4. Update the Word report using `report/LESSON_TEMPLATE.md`.
5. Mark progress in `report/LESSON_STATUS.md`.

## Repository layout

- `report/` working templates and planning files for the final write-up
- `evidence/` raw screenshots, notes, and code snippets per lesson
- `fixes/` consolidated diffs, patches, or exported code changes
- `scripts/` helper scripts used during testing or verification
- `notes/` team workflow and project-level notes

## Security note

`jwt-token.txt` is intentionally ignored so local tokens do not get committed into the repository.
