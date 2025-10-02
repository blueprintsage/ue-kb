---
title: C1/k6 — isolate region
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Protect a small critical task region from stealing.
## Task
Use `tbb::this_task_arena::isolate` around a task set; time it.
## Acceptance
- [ ] Region maintains expected ordering/time; overall correctness.