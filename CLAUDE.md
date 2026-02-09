# CLAUDE.md — Project Instructions

## Overview

This is a markdown-based project management tracker for a small operations team managing multiple portfolio companies and deal workstreams. It is currently in Stage 1 (static files) with a roadmap toward a lightweight web app (see `Web_App_Plan.md`).

## Repository Structure

| File | Purpose |
|------|---------|
| `README.md` | Active task lists organized by project. This is the single source of truth for outstanding work. |
| `Archive.md` | Completed tasks with completion dates, stored in a markdown table. |
| `Click-Ins_Ops_Calendar.md` | Recurring task rules for Click-Ins (daily, weekly, monthly). |
| `Click-Ins_Feb2026_Calendar.html` | Generated visual calendar for February 2026. |
| `Web_App_Plan.md` | Strategic roadmap for evolving this into a web application. |

## Projects

There are six active projects (lists):

1. **Freight Brokerage** — Deal evaluation: market mapping, comps, transaction structuring
2. **Click-Ins** — Portfolio company operations: financial model, banking, tax, reconciliations
3. **Zamp** — Portfolio company finance: financial statements, bill processing, journal entries
4. **Stratix** — Business development outreach
5. **LWT** — Finance operations: credit card categorization, bill pay
6. **Independent Sponsor** — Deal review and feedback

## Task Management Rules

### Adding tasks
- Add new tasks to `README.md` under the correct project heading.
- Use `- [ ] Task description` format (unchecked markdown checkbox).
- Place new tasks at the end of the relevant project's list unless instructed otherwise.

### Completing tasks
- When a task is completed, do two things:
  1. Remove the task line from `README.md`.
  2. Add a row to the table in `Archive.md` with the project name, task description, and today's date (e.g., `Feb 9, 2026`).
- Never simply check the box (`[x]`); always move completed tasks to the archive.

### Archiving format
Use this table row format in `Archive.md`:
```
| Project Name | Task description | Mon DD, YYYY |
```

## Recurring Tasks (Click-Ins)

Recurring tasks are defined in `Click-Ins_Ops_Calendar.md` and should not be tracked as one-off items in `README.md`. They include:
- **Daily (1st of month):** Send invoices to customers
- **Weekly (Sundays):** Pull Valley Bank transactions and share with SourceIn team
- **Monthly (2nd to last business day):** Request invoicing detail from Barak; send invoice list to SourceIn

When generating or updating a monthly calendar HTML file, follow the existing format in `Click-Ins_Feb2026_Calendar.html` and color-code by frequency: blue = daily, green = weekly, yellow = monthly.

## Style and Conventions

- Keep task descriptions concise but specific (include names, companies, or deliverables when relevant).
- Use plain language; avoid jargon unless it is already used in the existing tasks.
- Maintain alphabetical order for the six project headings in `README.md` only if re-ordering is explicitly requested; otherwise preserve the current order.
- Date format: `Mon DD, YYYY` (e.g., `Feb 9, 2026`).

## What Not to Do

- Do not delete or overwrite `Web_App_Plan.md` unless asked. It is a planning document, not an active task file.
- Do not add recurring calendar tasks to `README.md`; those belong in `Click-Ins_Ops_Calendar.md`.
- Do not reorganize, rename, or restructure files without explicit instruction.
- Do not create new project headings in `README.md` without explicit instruction.
