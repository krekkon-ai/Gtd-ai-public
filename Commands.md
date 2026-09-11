# Commands

This file contains the short commands used jointly.

## Inbox / Processing

* `/inbox` – adds a new personal item to the `00_Inbox.md` file
* `/sisinbox` – adds a new work-related (ShipItSmarter) item to the `00_SiSInbox.md` file
* `/review` – processes the Inbox
* `/next` – shows the current Next Actions
* `/list` – lists all current Next Actions from the GitHub GTD system, including priority, estimated time, and Label
* `/ListInbox` – lists all unprocessed Inbox items based on the current `00_Inbox.md` file in GitHub

## Marking Tasks as Done

* `/done 1,2,3` – marks the specified numbered items as done
* `/done 1-5` – marks a range of numbered items as done
* `/done 40 minutes` – specifies the actual time spent on a completed task; both estimated and actual time must be recorded
* `/done 1 40 minutes` – marks the specified item as done and records the actual time spent
* The `/Done` and `/done` commands must be handled identically.
* If no actual time is provided in the done command, the AI must ask before closing the task: **"How long did it take?"**

## Time Estimates

For completed tasks, the AI preserves both the original estimated time and the actual time spent. These can later be analyzed to determine how accurate the time estimates are.

## Note

In the `/done` command, the numbers refer to the stable item numbers in the relevant project list.

When an item is completed, it is removed from the active list and moved to the completed items at the end of the list, but the intermediate item numbers do not change.

This ensures that every item retains the same ID over the long term.

Items marked as done receive an `x` marker on the appropriate project page, and in the personal GTD system they must also be preserved in the `99_Done.md` file.
