# Epics and Stories - Todo App Enhancements

## Epics

### MVP
- Epic: Task Data Model
- Epic: Filtered Views
- Epic: Local Persistence

### Post-MVP
- Epic: Visual Emphasis
- Epic: Sorting Enhancements

## Stories

### MVP
- Epic: Task Data Model
  - Story: Add due date field (optional ISO YYYY-MM-DD)
  - Story: Add priority field with default P3
  - Story: Enforce priority values P1/P2/P3 only
  - Story: Ignore invalid due dates (treat as absent)
  - Story: Require title on task creation
- Epic: Filtered Views
  - Story: Show All view including completed tasks
  - Story: Show Today view for incomplete tasks due today
  - Story: Show Overdue view for incomplete tasks past due
- Epic: Local Persistence
  - Story: Persist tasks with priority and due date locally
  - Story: Load tasks from local storage on startup

### Post-MVP
- Epic: Visual Emphasis
  - Story: Highlight overdue tasks visually
  - Story: Display color-coded priority badges (red P1, orange P2, gray P3)
- Epic: Sorting Enhancements
  - Story: Sort tasks overdue first, then by priority P1→P3
  - Story: Order remaining tasks by due date ascending, undated last

## Acceptance Criteria

_Omitted per instruction._

## Technical Requirements

_Omitted per instruction._
