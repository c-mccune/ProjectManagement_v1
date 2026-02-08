# Web App Plan — Project Management Tool

## Stage 1: Static Site (Current State)
GitHub Pages serves the HTML calendar and markdown files. Colleagues can view but not edit. Good enough if only one person is managing tasks.

## Stage 2: Shared Editing via GitHub
- Move the to-do lists and calendar into a simple frontend (HTML/JS) that reads from and writes to the repo via the GitHub API
- Colleagues get GitHub access and can check off tasks, add items
- Git history gives a free audit trail of who changed what and when
- **Limitation:** requires everyone to have GitHub accounts

## Stage 3: Lightweight Web App
This is where it becomes a real tool.

### Frontend
- A single-page app (React, Vue, or even plain HTML/JS) with views for: project list, per-project to-do list, ops calendar, archive
- Color-coded calendar view like the HTML file, but interactive

### Backend
- A simple API (Node/Express, Python/Flask, etc.) or go serverless (Vercel/Supabase)
- Database: PostgreSQL or even SQLite to start

### Data Model
- `projects` — Freight Brokerage, Click-Ins, Zamp, Stratix, LWT, Independent Sponsor
- `tasks` — linked to a project, with status (open/completed), created/completed dates
- `calendar_rules` — recurring task definitions (day of month, day of week, relative rules like "2nd to last business day")
- `archived_tasks` — completed tasks with timestamps

### Core Features (Build First)
1. Dashboard showing all 6 projects with task counts
2. Per-project task list with add/complete/archive
3. Ops calendar with recurring rule engine ("every Sunday", "2nd to last business day" logic)
4. Generated monthly calendar view from those rules
5. User accounts so colleagues can log in

### Features to Add Later
- Slack notifications (via Slack webhook API)
- Assignment (who owns each task)
- Due dates and reminders
- Comments/notes per task

## Stage 4: Consider Existing Platforms
Before building custom, consider whether tools like Notion, Linear, or Asana could handle this. The use case has two things that are somewhat unique:
- **Ops calendar with rule-based recurring tasks** (most tools handle simple recurrence but not "2nd to last business day")
- **Per-project structured notes** (Slack messages, naming conventions tied to tasks)

If those are important, a custom app is justified. If not, Notion with databases could cover 80% of this.

## Recommendation
For a small team (< 10 people), start at Stage 3 with a minimal web app. The data model is simple, the calendar logic is the most interesting part, and it could be built in a few hours.
