# Waiting For

## Purpose

`Waiting For` contains commitments or outcomes that the user is waiting to receive from another person, team, company, service, or external dependency.

An item belongs here when **someone else must act before the user can continue**.

It should not be used as a general reminder list for actions that the user can already take themselves.

## Waiting For Items

| # | Waiting For | From | Date Added | Follow-up / Constraint | Status |
|---:|---|---|---|---|---|
| 1 | Reply to the project proposal | Alex | 2026-09-08 | Follow up if no reply by Friday | Waiting |
| 2 | Confirmation of the service appointment | Service provider | 2026-09-09 | Appointment needed before planning next step | Waiting |
| 3 | Delivery of the replacement part | Supplier | 2026-09-10 | Check tracking if delayed | Waiting |
| 4 | Feedback on the draft document | Project team | 2026-09-10 | Needed before final version | Waiting |

## Processing Rules

When adding an item to `Waiting For`:

- Record **what outcome is being awaited**.
- Record **who or what it is waiting on**.
- Record the **date it was added** when useful for follow-up.
- Capture any known **follow-up point, deadline, or constraint**.
- Do not create a duplicate Next Action while the action is genuinely blocked by another person or external dependency.

When processing an existing Waiting For item:

1. **Is it still genuinely waiting on someone else?**
   - If yes, leave it here.
   - If no, remove it and process the next action normally.

2. **Has the expected response, delivery, or decision arrived?**
   - If yes, remove the Waiting For item and process whatever became actionable.
   - If the result creates a Next Action, add it to the appropriate place.
   - If it creates a project step, update the relevant project page and project index as required.

3. **Does a follow-up need to happen?**
   - If the user now needs to take action, create the concrete Next Action in `01_NextActions.md`.
   - If the follow-up is tied to a specific date or time, use `85_Calendar.md` instead.

4. **Is the item no longer relevant?**
   - Remove it rather than keeping stale waiting items in the system.

## Follow-up Principle

A Waiting For item should make it easy to answer:

> **What am I waiting for, from whom, and when should I check again?**

Waiting For is a tracking list, not a task list. The user should not need to repeatedly remember to check it; the information in the entry should be sufficient to support the next review or follow-up action.

## Weekly Review

During the Weekly Review, review every Waiting For item and check:

- Is it still genuinely pending?
- Has the expected response or delivery already happened?
- Is the responsible person or organization still correct?
- Does a follow-up need to be sent?
- Has the waiting item become a Next Action, Calendar item, project step, or something that should be removed?

Keep `80_WaitingFor.md` current so that anything blocked by another party is visible and trusted rather than being kept in the user's head.
