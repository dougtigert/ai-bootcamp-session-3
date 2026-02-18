# Functional Requirements for TODO App

This document captures the MVP and Post-MVP functional scope based on the Sept 16 requirements meeting and Sept 17 Slack confirmations.

## MVP Functional Requirements

- Task fields:
	- `title`: required.
	- `priority`: enum `P1 | P2 | P3`; default `P3` when unspecified.
	- `dueDate`: optional ISO `YYYY-MM-DD`; invalid values are ignored (treated as absent).
- Filters (views):
	- **All**: shows all tasks, including completed.
	- **Today**: shows only incomplete tasks due today.
	- **Overdue**: shows only incomplete tasks with due date before today.
- Storage: local-only; no backend or external storage.

## Acceptance Criteria (MVP)

- Priority default:
	- When creating a task without an explicit `priority`, it is stored as `"P3"`.
	- `priority` only accepts `"P1"`, `"P2"`, or `"P3"`.
- Due date validation:
	- `dueDate` accepts ISO `YYYY-MM-DD` strings.
	- Invalid `dueDate` values are ignored (task is treated as undated).
- Filters behavior:
	- **All** view includes completed tasks.
	- **Today** and **Overdue** views exclude completed tasks.
	- **Today** includes tasks with `dueDate` equal to the current date.
	- **Overdue** includes tasks with `dueDate` earlier than the current date.
- Persistence:
	- Tasks (including `priority` and `dueDate`) persist via local storage.

## Post-MVP Functional Requirements

- Overdue highlighting: visually distinguish overdue tasks (e.g., red styling).
- Sorting rules: overdue first → priority (P1→P3) → due date ascending → undated last.
- Priority badges: color-coded UI (e.g., red=P1, orange=P2, gray=P3) for clarity.

## Out of Scope

- Notifications.
- Recurring tasks.
- Multi-user features.
- Keyboard navigation.
- External storage/backends.

## References

- PRD: [docs/prd-todo.md](docs/prd-todo.md)
- Requirements meeting: [docs/artifacts/09162025-requirements-meeting.vtt](docs/artifacts/09162025-requirements-meeting.vtt)
- Slack confirmation: [docs/artifacts/09172025-slack-conversation-export.txt](docs/artifacts/09172025-slack-conversation-export.txt)
- Related story: [docs/stories/priority-field-story.md](docs/stories/priority-field-story.md)
