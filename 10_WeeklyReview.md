# Weekly Review

A weekly review keeps the GTD system current, complete, and trustworthy. The goal is to get clear, get current, and get creative so the system can be trusted for the week ahead.

## 1. Prepare

- Choose a time and place where the review can be completed without interruption.
- Gather any loose notes, reminders, messages, or other inputs that are not yet in the GTD system.
- Make sure the GitHub repository is available; **GitHub is the primary source of truth for the GTD system.**

## 2. Get Clear — Empty the Inbox

Review every item in `00_Inbox.md` until there are no unprocessed items left.

For each Inbox item, follow the GTD processing sequence:

1. **What is it?** Clarify what the item actually means.
2. **Is action required?**
   - No action → Trash, Someday / Maybe, or Reference.
   - Action required → continue processing.
3. **What is the desired outcome?** If it requires multiple steps, identify the project and desired outcome.
4. **What is the next action?** Define one concrete, physical, executable next step.
5. **What label applies?** Every Next Action must have a Label.
6. **Is it under two minutes?** Do it immediately rather than organizing it as a separate task.
7. Put the processed item in the correct place: project, `01_NextActions.md`, `80_WaitingFor.md`, `85_Calendar.md`, `Someday/`, or reference material.

After processing, remove the item from `00_Inbox.md`.

## 3. Get Clear — Review Projects

Review `Projects/00-Projects.md` and every active project page.

For each project:

- Confirm the desired outcome is still clear and relevant.
- Confirm the project is still active.
- Confirm there is **at least one concrete Next Action**.
- Make sure the current Next Action is actually actionable and not a vague project description.
- Check that the project index contains **exactly one current Next Action** for the project.
- Check that the project index uses the current Next Action's priority and estimated time.
- Do not invent missing priority, estimated time, or total project time; keep missing values as `—` or ask the user when required.
- Make sure additional project-specific Next Actions remain on the project page and are not duplicated in `Projects/00-Projects.md`.
- Re-sort the project index by current Next Action priority, then by shorter estimated time.

If a project has no remaining Next Action, do not invent one. Check whether the project is complete or whether the user needs to define the next step.

## 4. Get Clear — Review Next Actions

Review `01_NextActions.md` from top to bottom.

For every Next Action, check:

- Is it still a valid and meaningful action?
- Is it concrete, physical, and executable?
- Is the Label still correct?
- Is the priority still appropriate?
- Is the estimated time still realistic?
- Is there a time or other constraint that should be recorded?
- Does it belong to an active project instead of being a standalone Next Action?

Keep standalone Next Actions in `01_NextActions.md`. Project-specific Next Actions belong on their project pages, with only the current one surfaced in `Projects/00-Projects.md`.

## 5. Get Clear — Review Waiting For

Review `80_WaitingFor.md`.

For every waiting item:

- Is it still genuinely waiting on someone else?
- Is the responsible person or organization clear?
- Has the expected response or delivery already happened?
- Does a follow-up need to be sent?
- If the response has arrived, process the resulting action and remove the waiting item.

Add a Next Action or calendar entry when follow-up is now appropriate.

## 6. Get Clear — Review Calendar

Review `85_Calendar.md` with the upcoming weeks in view.

Look for:

- fixed appointments and hard landscape commitments
- deadlines and time-specific actions
- preparation needed for upcoming appointments or events
- overdue or missed commitments
- actions that belong on a specific date or time rather than in Next Actions

Move only genuinely time-specific actions to the calendar. Do not use the calendar as a general task list.

## 7. Get Clear — Review Routines

Review `02_Routines.md`.

Check whether:

- routines are still relevant and useful
- recurring responsibilities are represented consistently
- obsolete routines should be removed or changed
- recurring work has accidentally been stored as one-off Next Actions

Keep routine information in `02_Routines.md`, not in the Inbox or as duplicated one-off tasks unless a specific execution is needed.

## 8. Get Clear — Review Someday / Maybe

Review the `Someday/` lists.

For each item, decide whether it should:

- remain Someday / Maybe
- become an active project
- become a Next Action
- be moved to another appropriate place
- be deleted because it is no longer relevant

Pay particular attention to items that have become timely or important.

## 9. Get Clear — Review Done and Time Calibration

Review recent entries in `99_Done.md`.

Look for patterns between:

- estimated time
- actual time
- repeated overestimation or underestimation

Use these data points to improve future estimates. Completed tasks should retain both the original estimate and actual time.

## 10. Get Current — Check System Integrity

Before finishing the review, verify that the system is internally consistent:

- `00_Inbox.md` contains only unprocessed items.
- Every active project has a Next Action.
- `Projects/00-Projects.md` contains one current Next Action per active project.
- Standalone Next Actions are in `01_NextActions.md`.
- Waiting items are in `80_WaitingFor.md`.
- Time-specific commitments are in `85_Calendar.md`.
- Routines are in `02_Routines.md`.
- Someday / Maybe items are in the `Someday/` area.
- Completed work is in `99_Done.md`.
- No item is duplicated unnecessarily across lists.
- GitHub reflects the current trusted state of the system.

## 11. Get Creative — Review Horizons

Once the system is current, step back and look beyond individual tasks.

Review:

- active projects and desired outcomes
- upcoming commitments and deadlines
- areas of responsibility that may be missing a project or Next Action
- Someday / Maybe ideas worth reconsidering
- anything that is causing recurring friction, stress, or ambiguity

Ask: **What is missing from the system that I need to capture?**

## 12. Choose the Week's Focus

Only after the system is clear and current, decide what deserves attention in the coming week.

Use:

- priorities
- upcoming calendar commitments
- available time
- energy
- context / Label
- project momentum

The weekly focus is a guide for choosing actions, not a replacement for the complete GTD system.

## Weekly Review Completion Checklist

- [ ] Inbox is empty or every remaining item has been intentionally clarified.
- [ ] Every active project has a clear desired outcome and at least one Next Action.
- [ ] Project index contains exactly one current Next Action per project.
- [ ] Next Actions are concrete, current, and correctly labeled.
- [ ] Waiting For items are current and actionable follow-ups are identified.
- [ ] Calendar has been reviewed for upcoming commitments and preparation.
- [ ] Routines have been reviewed.
- [ ] Someday / Maybe has been reviewed.
- [ ] Recent Done items have been reviewed for estimate calibration.
- [ ] System integrity has been checked.
- [ ] The coming week's focus is clear.

## Core Principle

The Weekly Review is complete when the GTD system can be trusted again: **nothing important is trapped in your head, commitments are captured in the right place, projects have clear next steps, and the system is current enough to support confident choices.**
