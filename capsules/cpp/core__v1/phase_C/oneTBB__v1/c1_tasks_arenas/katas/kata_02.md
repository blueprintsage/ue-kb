---
title: C1/k2 — task_group two tasks
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Spawn two independent tasks and wait.
## Task
`task_group g; g.run(f1); g.run(f2); g.wait();` verify both effects occurred.
## Acceptance
- [ ] Both tasks complete; shared state matches expected.