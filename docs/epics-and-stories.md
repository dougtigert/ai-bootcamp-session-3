# Epics and Stories - Todo App Enhancements

## MVP
- Epic: Task Data Model
  - Story: Add due date field (optional ISO YYYY-MM-DD)
    - Acceptance: Tasks accept `dueDate` in `YYYY-MM-DD`; field may be empty.
  - Story: Add priority field with default P3
    - Acceptance: When no priority provided, task is stored as `P3`.
  - Story: Enforce priority values P1/P2/P3 only
    - Acceptance: Only `P1`, `P2`, `P3` are persisted/accepted.
  - Story: Ignore invalid due dates (treat as absent)
    - Acceptance: Invalid `dueDate` values are discarded and stored as no date.
  - Story: Require title on task creation
    - Acceptance: Task creation fails or is blocked when title is empty/whitespace.
- Epic: Filtered Views
  - Story: Show All view including completed tasks
    - Acceptance: All view lists both completed and incomplete tasks.
  - Story: Show Today view for incomplete tasks due today
    - Acceptance: Today view lists only incomplete tasks with `dueDate` equal to current date.
  - Story: Show Overdue view for incomplete tasks past due
    - Acceptance: Overdue view lists only incomplete tasks with `dueDate` earlier than current date.
- Epic: Local Persistence
  - Story: Persist tasks with priority and due date locally
    - Acceptance: Saved tasks retain `title`, `priority`, `dueDate`, `completed` in local storage.
  - Story: Load tasks from local storage on startup
    - Acceptance: On launch, tasks (with `priority` and `dueDate`) are restored from local storage.

## Post-MVP
- Epic: Visual Emphasis
  - Story: Highlight overdue tasks visually
    - Acceptance: Overdue tasks render with distinct highlighting (e.g., red styling).
  - Story: Display color-coded priority badges (red P1, orange P2, gray P3)
    - Acceptance: Tasks show priority badges with colors red=P1, orange=P2, gray=P3.
- Epic: Sorting Enhancements
  - Story: Sort tasks overdue first, then by priority P1→P3
    - Acceptance: List order places overdue tasks above others, ordered P1→P3.
  - Story: Order remaining tasks by due date ascending, undated last
    - Acceptance: Non-overdue tasks sort by due date ascending, with no-due-date last.
