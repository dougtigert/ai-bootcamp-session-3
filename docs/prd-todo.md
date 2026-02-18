# Product Requirements Document (PRD) - Todo App Enhancements (Due Dates, Priorities, Filters)

## 1. Overview

We are upgrading the basic Todo app (currently title + completed) to support due dates, priority levels, and filter views so users can better organize tasks and focus on what’s urgent. The MVP is intentionally lightweight and uses local storage only to keep the solution teachable and simple.

---

## 2. MVP Scope

- Add `dueDate` (optional) in ISO `YYYY-MM-DD` format.
- Add `priority` enum: `P1 | P2 | P3`; default `P3` if unspecified.
- Add filter views: **All**, **Today**, **Overdue**.
- Filter behavior: **All** includes completed tasks; **Today** and **Overdue** show only incomplete tasks.
- Storage remains local-only; no backend or external services.
- Validation and data model:
  - `title`: required.
  - `priority`: must be one of `P1 | P2 | P3`; default to `P3` when absent.
  - `dueDate`: optional ISO date; invalid values are ignored (treated as absent).

---

## 3. Post-MVP Scope

- Overdue tasks are visually highlighted (e.g., red styling) to stand out.
- Sorting rules: overdue first → priority (P1→P3) → due date ascending → tasks without a due date last.
- Priority badges with color-coded styling (e.g., red=P1, orange=P2, gray=P3) as UI polish.

---

## 4. Out of Scope

- Notifications.
- Recurring tasks.
- Multi-user features.
- Keyboard navigation.
- External storage/backends (remain local-only).

---

## 5. Data Model & Validation (MVP)

- `title`: required.
- `priority`: `"P1" | "P2" | "P3"`; default `"P3"` if not provided.
- `dueDate`: optional ISO `YYYY-MM-DD`; invalid values are ignored (treated as absent).

## 6. Filters Behavior

- **All**: shows all tasks, including completed.
- **Today**: shows only incomplete tasks with `dueDate` equal to the current date.
- **Overdue**: shows only incomplete tasks with `dueDate` earlier than the current date.

## 7. Visual Design Guidance

- Priority badges: color-coded to distinguish urgency (e.g., red=P1, orange=P2, gray=P3).
- Overdue highlighting: visually emphasize overdue tasks (e.g., red styling).

## 8. Sorting (Post-MVP)

- Order tasks: overdue first → priority (P1→P3) → due date ascending → undated last.

References: Sept 16 Requirements Meeting (VTT) and Sept 17 Slack confirmations.
