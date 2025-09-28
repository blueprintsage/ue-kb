---
title: C1/k7 — nested parallel
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Run `parallel_for` inside an arena execute without deadlocks.
## Task
`arena.execute([&]{ parallel_for(...); });`
## Acceptance
- [ ] Completes; no deadlock; results correct.