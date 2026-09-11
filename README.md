# GTD AI

This repository is the foundation of a personal, AI-assisted GTD system.

The system uses GitHub as the source of truth for personal GTD data. The AI acts both as a GTD coach and as an agent that maintains the files and keeps the system synchronized.

## Core principles

- The Inbox is the capture point for unprocessed ideas, tasks, requests, and reminders.
- Inbox items are processed through the GTD decision process rather than simply being converted into tasks.
- Every active project has a Desired Outcome and at least one concrete Next Action.
- Larger projects have their own project page under `Projects/`.
- The project index contains only the single current Next Action for each active project.
- Completed tasks are moved to `99_Done.md` together with their original estimate and actual time spent.
- Time estimates are tracked so they can be calibrated over time.
- Git commit history preserves the history of changes.
- The goal is not perfect GTD, but stress-free operation with as little administration as possible.

## Current structure

### Capture and action lists

- `00_Inbox.md` – personal, unprocessed Inbox items
- `00_SiSInbox.md` – work-related ShipItSmarter Inbox items
- `01_NextActions.md` – current concrete Next Actions, with priority, estimated time, and Label
- `02_Routines.md` – recurring routines
- `80_WaitingFor.md` – items delegated to or waiting on other people
- `85_Calendar.md` – time-specific items that belong on the calendar
- `99_Done.md` – completed tasks, including estimated and actual time where available

### Reviews and instructions

- `10_WeeklyReview.md` – weekly review
- `Commands.md` – the shared short commands used to operate the system
- `AGENT_INSTRUCTIONS.md` – detailed rules for the AI agent and GTD processing

### Projects

- `Projects/00-Projects.md` – index of all active projects
- `Projects/` – individual project pages

The project index is intentionally lightweight: each project appears once and shows only its current Next Action, together with its priority and estimated time. Additional project steps remain on the project's own page.

### Someday

- `Someday/` – ideas and items that are not actionable now but may become relevant later

## Labels

Every Next Action has a Label describing its context or type. The current stable categories are:

- DIY
- Office
- Garden
- Animals
- Administration
- Shopping
- Digital
- Tidying
- Home

Shopping includes both buying and selling. Animals includes tasks related to cats, birds, bees, and other animals. DIY is preferred for physical home tasks involving installation, repair, construction, painting, or similar work.

## GTD processing

When something is captured in the Inbox, the AI processes it in this order:

1. Clarify what it is.
2. Decide whether it requires action.
3. If not actionable, route it to Trash, Someday, or Reference as appropriate.
4. If actionable, determine the Desired Outcome when multiple steps are involved.
5. Define the next concrete, physical, executable action.
6. Assign a Label to the Next Action.
7. Apply the two-minute rule.
8. Place the item in the appropriate part of the system and remove the processed item from the Inbox.
9. If it belongs to a project, verify that the project has a clear Next Action.

## Projects

Each active project is listed in `Projects/00-Projects.md` and, when appropriate, has its own project page.

A project page may contain multiple future tasks / Next Actions, but only the current Next Action is shown in the project index.

The project index is ordered by:

1. Next Action priority, with P1 highest and P10 lowest.
2. For equal priorities, shorter Next Action estimated time comes first.

The project's total estimated time is stored separately and is not used for ordering the index.

When a project's current Next Action is completed, the AI moves it to `99_Done.md`, records the actual time, updates the project page, pulls the next Next Action into the project index, and re-sorts the index.

If a project has no further Next Action, the index indicates this rather than inventing a new action.

## Time tracking

Completed tasks preserve both:

- **Estimated time** – the original estimate.
- **Actual time** – the time actually spent.

Example:

`Fine-tune the back door lock — estimate: 30 minutes — actual: 40 minutes`

These data points can later be used to improve future estimates and GTD coaching.

## Commands

The main commands are documented in `Commands.md`, including:

- `/inbox` – capture a personal Inbox item
- `/sisinbox` – capture a ShipItSmarter Inbox item
- `/review` – process the Inbox
- `/next` – show current Next Actions
- `/list` – list all current Next Actions with priority, estimated time, and Label
- `/ListInbox` – list all unprocessed personal Inbox items
- `/done` / `/Done` – mark items complete and record actual time

See `Commands.md` for the complete command reference.

## Special project: Garden

The Garden is treated as a large project. It does not move to Someday; its long-term tasks remain on the project page.

## Operating philosophy

The AI should keep the system simple, ask when something is unclear, avoid unnecessary administration, preserve information, help break down projects, and provide clear feedback when work is completed.

**The goal is not perfect GTD. The goal is stress-free operation.**
