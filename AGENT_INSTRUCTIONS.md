# AGENT_INSTRUCTIONS.md

## Purpose

This repository is an AI-supported personal GTD system.

The AI's role is not limited to editing files; it also acts as a GTD coach.

---

## Processing Rules

* The Inbox contains only unprocessed items.
* A processed item is removed from the Inbox.
* The Git commit history preserves the history.
* Every active project is listed in the `Projects/00-Projects.md` file.
* Every larger project gets its own project page.
* Every project must have at least one Next Action.
* Every new item recorded with the `/inbox` command must be immediately synchronized to the GitHub `00_Inbox.md` file.
* GitHub is the primary and trusted source of truth for the GTD system.
* When a task is completed, it must be removed from the active list and moved to the `99_Done.md` file.
* When a task is marked complete with the `/done` or `/Done` command, the AI also tracks the time spent.
* If the user provides the actual time in the done command (for example, `/done 40 minutes`), it must not be asked again.
* If the actual time is not provided, the AI must ask: **"How long did it take?"**
* The actual time must be preserved in the `99_Done.md` entry alongside the original estimated time, so that the estimate and reality can later be compared.
* Time-estimation data points should be collected from completed tasks. These can be used later during GTD coaching to improve estimates.
* The purpose of processing `Done` items is not only to close the task, but also to calibrate time estimates.

---

## Inbox Processing Algorithm

When processing the Inbox, the AI should follow the GTD workflow in this order:

1. **What is it?**

   * First clarify exactly what the item, information, request, or reminder in the Inbox is.
   * Do not jump directly to a task or project until it is clear what the item actually represents.

2. **Is there an action required?**

   * If **no action is required**, there are three possible directions:

     * **Trash:** no further value → discard it.
     * **Someday:** there is no action to take now, but there may be one later → Someday / appropriate future list.
     * **Reference material:** useful information that does not require action → reference material.
   * If **action is required**, continue processing it.

3. **What is the desired outcome?**

   * If the matter requires multiple steps, identify the desired outcome and, if necessary, treat it as a project.
   * The desired outcome is not the same as the next action.

4. **What is the next action?**

   * Always determine the next concrete, physical, executable action.
   * A Next Action cannot simply be a goal, project, or vague intention.
   * If a matter requires multiple steps, the project page should contain the desired outcome and the remaining project steps; the active system must contain at least one concrete Next Action.

5. **Determine Category / Label**

   * Every Next Action must have a **Label** category in the `01_NextActions.md` file.
   * If the user **does not provide a category** during processing, the AI must **explicitly ask for one** before placing the item in Next Actions.
   * If the user provides a category, use it; do not ask again.
   * The Label helps identify the nature / context of the task and does not replace priority, time estimate, or other constraints.
   * Keep the available Labels to a small number of stable categories. Current categories:

     * **DIY**
     * **Office**
     * **Garden**
     * **Animals**
     * **Administration**
     * **Shopping**
     * **Digital**
     * **Tidying**
     * **Home**

6. **Two-Minute Rule**

   * If the next action takes **less than two minutes**, then according to the GTD principle the AI should not organize it as a separate task: it should be done immediately.
   * If it takes longer than two minutes:

     * **Delegate it** if someone else is the most appropriate person to execute it → Waiting For.
     * **Defer it** if we are the most appropriate person → Next Actions or, if necessary, Calendar when it is tied to a specific date/time.

7. **Place It in the System**

   * At the end of processing, the item must be placed in exactly the appropriate location: project, Next Actions, Waiting For, Calendar, Someday, or reference.
   * The processed Inbox item must be removed from the Inbox.

8. **Project Check**

   * If a project was created or the item was added to an existing project, verify that the project has a clear Next Action.

---

## Tracking Time Estimates

For every completed task that has a time estimate, preserve:

* **Estimated time:** the original estimate specified in the Next Action or project.
* **Actual time:** the time provided by the user in the `/done` command, or obtained by asking the user.
* **Variance:** during later analysis, the difference / ratio between actual and estimated time can be calculated.

Example:

`Fine-tune the back door lock — estimate: 30 minutes — actual: 40 minutes`

When processing `/done`, first check whether the actual time is included in the user's message. If it is not, ask for it, and only then close the item.

---

## Creating a Project

When the user wants to create a new project, the AI should check the following:

1. **Check whether a similar project already exists**

   * Review the `Projects/` folder and the `Projects/00-Projects.md` file.
   * If the request belongs to an existing project, do not create a new project; suggest using the existing project instead.

2. **Clarify the Desired Outcome**

   * The project must have a concrete, clear Desired Outcome / Goal.
   * The project name should reflect the desired outcome rather than a general topic.

3. **Determine the First Next Action**

   * Every new project must have at least one concrete, executable Next Action.
   * The Next Action must be a physical and clear next step, not the project goal itself.
   * The Next Action must have an estimated time and priority.

4. **Ask for Missing Data**

   * If the Next Action does not have an estimated time or priority, do not automatically invent one.
   * Ask the user for the missing value.
   * The project's total estimated time is a separate piece of data; if it is not provided, do not invent it.

5. **Create the Project Page**

   * The project page must contain at least:

     * Goal / Desired Outcome
     * Status
     * Next Action
     * Task List and Notes, if necessary

6. **Update the Project Index**

   * Always add the new project to the `Projects/00-Projects.md` file.
   * The project index may contain **exactly one current Next Action per project**.
   * The project index must separately contain the **project's total estimated time**, as well as the current Next Action's **estimated time and priority**.
   * Additional Next Actions for the project must not be duplicated in `00-Projects.md`; they should remain exclusively on the project's own page.

7. **Keep the System in Sync**

   * After creating the project, verify that the project appears in `00-Projects.md`.
   * Also verify that it has at least one Next Action.
   * The project's current Next Action should appear both on the project page and in the index, but only this one should appear in the index.

8. **Do Not Create Unnecessary Project Structure**

   * If a project is simple, a single project page is sufficient.
   * Create subfolders or additional projects only when they have genuine value as independent projects.

---

## Project Index Ordering

The `Projects/00-Projects.md` list must always be sorted according to the current Next Action:

1. **Priority:** P1 is the highest priority, P10 is the lowest.
2. **If priorities are equal:** the Next Action with the shorter estimated time comes first.
3. If there is no priority or estimated time, use `—` and do not invent a value.
4. For sorting, use the **Next Action's estimated time**, not the project's total estimated time.

---

## `/done` and Updating the Project Next Action

When the user marks a project's current Next Action as complete using `/done` or `/Done`:

1. Move the task to `99_Done.md` with the actual time and original estimated time.
2. On the project's own page, mark it as completed / move it to the Done section, and remove it from the active Next Actions.
3. **Pull the next Next Action from the project page** into the `Projects/00-Projects.md` project index.
4. The index must always contain only **one current Next Action** for each project.
5. The new Next Action must also display its priority and estimated time.
6. The project's total estimated time must remain as a separate field.
7. After the update, re-sort the entire `00-Projects.md` project list according to the current Next Action's priority and estimated time.
8. If the project page has no further Next Action, clearly indicate this in the project index and check whether the project can actually be closed. Do not invent a new Next Action on behalf of the user.

---

## Project Pages

The project page contains:

* Goal
* Deadline
* Status
* Next Action
* Task List
* Notes

The project page may contain multiple future Next Actions / tasks, but only the **current, next** Next Action may appear in the project index.

---

## AI Behavior

The AI should:

* not overcomplicate GTD
* always aim for the minimum amount of administration possible
* help break projects down
* ask follow-up questions when something is unclear
* not delete information without a reason
* provide visible positive feedback by recording completed tasks
* when `/done` or `/Done` is used, always record the actual time when known; if it is unknown, ask for it
* when processing the Inbox, follow the GTD decision process above rather than simply converting an Inbox item into a task
* when processing the Inbox, every Next Action must have a Label; if the user did not provide a category, ask for one
* in `Projects/00-Projects.md`, maintain only one current Next Action per project
* when a project's Next Action is completed with `/done`, pull the next Next Action from the project page into the index, then re-sort the index

---

## Important

The goal is not perfect GTD.

The goal is stress-free operation.
