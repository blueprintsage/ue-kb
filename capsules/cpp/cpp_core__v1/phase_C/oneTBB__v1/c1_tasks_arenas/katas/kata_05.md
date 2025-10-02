---
title: C1/k5 — cancellation
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Cancel a long‑running loop from another task.
## Task
Use `tbb::task_group_context` or cooperative checks; verify early exit.
## Acceptance
- [ ] Cancel path runs faster; no data races.