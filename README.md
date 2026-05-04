# ICS344 DVSA Project

This repository is organized for a report-first workflow.

Use the Word/Google Docs report as the polished deliverable, and use this repo to store:

- code and configuration changes
- raw screenshots and logs
- exact commands used
- lesson-by-lesson notes

## Suggested workflow

1. Reproduce one lesson.
2. Save raw evidence under `evidence/lesson X`.
3. Apply the fix and save code/config notes under that lesson folder.
4. Keep the final written report in `report/` when it is ready.
5. Keep the final slide deck in `presentation/`.

## Repository layout

- `report/` final written report output when ready
- `presentation/` final slide deck
- `evidence/` raw screenshots, notes, and code snippets per lesson

## Security note

`jwt-token.txt` is intentionally ignored so local tokens do not get committed into the repository.
The course handout PDFs are also ignored because the submitted repo should focus on the team's evidence and fixes.
