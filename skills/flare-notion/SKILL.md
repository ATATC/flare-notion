---
name: flare-notion
description: Maintain FLARE lab Notion project pages and Master Tasks, including FLARE T3 Summary Paper. Use when creating, organizing, estimating, assigning, updating, or completing tasks in this workspace; enforce required properties, calibrate estimates from completed work, record actual effort, and keep every actionable step as a top-level Master Task.
---

# FLARE Notion

Maintain task records in the user's existing Notion project-management system. Apply these rules to the tasks within the requested scope; do not silently audit or rewrite unrelated projects.

## Workspace and access

- [Master Tasks](https://app.notion.com/p/8e4393cf67ef4ca08fdbf7b573435b96) is the canonical task database.
- [FLARE T3 Summary Paper](https://app.notion.com/p/3f3e77d20a408046a061f0b2bc1a5a0e) is the project used to establish this workflow. Use the project specified in the current request; do not route every task here.
- Prefer an available Notion connector. Otherwise use the documented computer-use tools with the existing Notion session. Inspect current records and property options before editing; links and past observations are context, not proof of current state.
- Update records and page content within scope. Preserve the database schema, formulas, views, sharing, and permissions. Reuse existing people and select options.

## Every actionable step is a Master Task

- Create every task, including small steps, as its own record in Master Tasks at the same level.
- Keep `Parent task` empty. Do not create subtasks, nested task pages, or actionable checklists inside another task's body.
- Connect each record to its `Project`. A project page may display a linked view of Master Tasks; that does not make its records subtasks.
- Use a concrete action and deliverable in the title. Number titles only when ordering helps. Express dependencies through links or explanatory context, not parent-child nesting.
- Task bodies may contain scope, sources, rationale, acceptance criteria, and results. If a body contains separately actionable work, represent that work as peer Master Tasks instead.
- When converting existing embedded steps, check for matching records first. Create or reuse the peer tasks, verify them, then replace the old actionable checklist with links or reference context. Preserve useful notes and avoid duplicate work records.

## Required properties

Every task created or maintained must have all six fields populated. Preserve valid existing values unless the user asks to change them; fill missing values within the task's authorized scope.

| Field | Rule |
| --- | --- |
| `Category` | Choose the existing option that describes the work. For example, `Analysis` for evidence extraction and checks, `Writing` for drafting and revision. Avoid incidental or duplicate selections. |
| `Owner` | Use the requested assignee or the established owner of this work. For the requesting user's own work, identify that user and verify the matching person in Notion. Do not assume the repository author, skill installer, or project lead owns every task; do not assign collaborators without a basis. |
| `Priority` | Use explicit urgency, deadlines, and dependencies. Preserve an existing valid priority; for a new routine task without an urgency signal, use the existing `Medium` option and disclose that assumption briefly. |
| `Stage` | Reflect observed or user-reported progress. New unstarted work uses the existing `To do` option. Preserve ongoing/completed states unless the request supports a transition. |
| `Expected time (h)` | Enter a numeric estimate of focused work hours, calibrated from completed tasks as described below. |
| `Time required` | Select the corresponding existing duration option. This is a planning estimate, not the actual duration. |

If a required value cannot be inferred responsibly (especially the owner), ask one concise question and continue independent work. Do not invent a person or report the task as fully maintained while a required field is missing.

## Calibrate expected effort from completed work

1. Inspect recent completed tasks with recorded actual durations. Prefer similar scope, deliverable, category, owner, and project. Use actual effort, not their old estimates or time spent in a status.
2. Use the median actual duration of comparable tasks as a practical starting point. Adjust for concrete scope differences, source availability, and uncertainty. When helpful, compare their actual-to-estimated ratios to detect systematic overestimation or underestimation; do not apply the same correction twice.
3. Record the calibrated value in `Expected time (h)` and its matching `Time required` option. If exact hours fall between available options, retain the exact numeric estimate and choose the nearest suitable bucket, noting the rounding. Do not create new options merely to encode a duration. Verify the workspace's convention before converting day/week buckets to hours.
4. Briefly state the calibration basis (comparable records, observed duration, and adjustment) in the task's context or the user-facing update. With sparse history, label the estimate provisional; use the closest evidence and explain the limitation.
5. Preserve historical estimates on completed tasks so future calibration remains meaningful. Re-estimate unfinished work when requested or when the maintenance scope includes planning updates. Do not replace an estimate with an actual duration just because a task finished.

Calibration example from the initial FLARE T3 workflow (2026-10-15): one contributor reported **1 hour each** for source verification, five team method sections, and cross-checking. For similar work by that contributor with similar preparation, this evidence should inform future estimates instead of blindly retaining the original two-hour drafting estimates. Refresh the actual records and select comparable work for the current owner; this example is not a universal one-hour default or a report of current task status.

## Completion requires actual time

- When asked to mark a task completed, obtain its actual focused work duration from the user's report or a reliable work-time record. A prior estimate, page-edit timestamp, calendar span, model runtime, or another task's duration is not evidence of this task's actual effort.
- If actual time is missing, ask how long the task took. Prepare other updates while awaiting the answer; do not invent the duration or finalize the completion transition without it.
- Write the duration to `Actual time (h)` and the corresponding `Actual time required` option, then set `Stage` to the workspace's completion status. Prefer a single atomic update where supported; otherwise save actual time before the completion status.
- Treat `Actual hours` and `Hours` as derived fields when the current schema identifies them as formulas. Do not edit formulas to force a value. Verify their results where relevant.
- For already-completed tasks with missing actuals, backfill from the user's report without reopening them. If the user says “1 hour for the completed ones,” inspect current statuses and apply one hour to each completed task in the referenced set, not to ongoing tasks or unrelated completed work.
- Keep estimates and actuals distinct. If their duration buckets cannot express the exact actual, preserve the exact value in `Actual time (h)` and explain the bucket rounding.

## Reliable updates and verification

- Before creating records, inspect for duplicates. Before editing, read the latest values so concurrent user updates are preserved.
- In computer-use workflows, target the property row by its exact name: `Time required` and `Actual time required` are different fields. A multi-select menu can remain open after selection. Explicitly close it and verify the saved value before opening another property or typing a number.
- Verify a number editor is the active dialog before filling it. Never type a duration into an option-search box or create an unintended category. After an interrupted action, inspect the record before retrying; do not blindly duplicate or repeat mutations.
- Read back each changed record: title, project, empty parent, six required properties, and actual-time fields for completed work. Resolve mismatched paired fields using the user's requested value and the documented rounding rule.
- Report the number of tasks changed, relevant effort totals, and any unresolved required values. Distinguish total planned effort, remaining work, and recorded actual effort. Follow the active tool's screenshot/evidence requirements when using the UI.
