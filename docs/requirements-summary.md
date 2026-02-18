# Requirements Summary

This summarizes the agreed MVP and Post-MVP scope for the Todo app enhancements based on the Sept 16 meeting transcript and Sept 17 Slack confirmation.

## MVP
- **Due Date:** Optional `dueDate` in ISO `YYYY-MM-DD` format.
- **Priority:** `priority` enum with values `P1`, `P2`, `P3`; default `P3`.
- **Filters:** Views for **All**, **Today**, **Overdue**.
- **Filter Behavior:** In **All**, show completed tasks; **Today** and **Overdue** show only incomplete tasks.
- **Storage:** Local-only; no backend or external storage changes.
- **Validation:**
  - `title` required.
  - `priority` must be one of `P1 | P2 | P3`; default to `P3` if absent.
  - `dueDate` optional; invalid dates are ignored (treated as absent).

## Post-MVP
- **Overdue Highlighting:** Visually distinguish overdue tasks (e.g., red styling).
- **Sorting Rules:** Order tasks as: overdue first → priority (P1→P3) → due date ascending → tasks without a due date last.

## Notes & Design Guidance
- **Priority Badges:** Color-coded badges for priority (e.g., red=P1, orange=P2, gray=P3) were requested in the meeting; treat as design guidance. Implement in MVP if feasible, otherwise include with Post-MVP polish.

## Out of Scope (Confirmed)
- Notifications.
- Recurring tasks.
- Multi-user features.
- Keyboard navigation.
- External storage/backends (stay local).
