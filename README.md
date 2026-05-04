# ICS344 DVSA Project

Final repository for the ICS344 DVSA course project.

This repo is organized around the submitted report and presentation, with lesson-by-lesson evidence kept for verification and traceability.

## Final deliverables

- `report/ICS344_Final_Report.pdf` final written report
- `presentation/ICS344_DVSA_Final_Presentation.pdf` final slide deck
- `evidence/` raw evidence, commands, observations, screenshots, and code snippets for lessons 1-10

## Evidence layout

Each lesson folder uses the same structure:

- `screenshots/` terminal, browser, AWS Console, CloudWatch, IAM, or service screenshots
- `notes/` commands used, observations, and validation notes
- `code/` fix snippets, policy snippets, or screenshots of relevant code/configuration changes

Lesson folders:

- `evidence/lesson 1` Event Injection
- `evidence/lesson 2` Broken Authentication
- `evidence/lesson 3` Sensitive Data Exposure
- `evidence/lesson 4` Insecure Cloud Configurations
- `evidence/lesson 5` Broken Access Control
- `evidence/lesson 6` Denial of Service
- `evidence/lesson 7` Over-Privileged Functions
- `evidence/lesson 8` Logic Vulnerabilities
- `evidence/lesson 9` Vulnerable Dependencies
- `evidence/lesson 10` Unhandled Exceptions

## Repository scope

The final report and slide deck are the polished submission artifacts. The evidence folders support the report by preserving the commands, outputs, screenshots, and fix references used during the project.

This repository does not include local secrets, JWT tokens, draft slide decks, or course handout PDFs. Those files are intentionally ignored in `.gitignore`.
