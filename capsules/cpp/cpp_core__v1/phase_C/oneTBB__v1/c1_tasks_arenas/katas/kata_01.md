---
title: C1/k1 — parallel_for sum
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Compute sum(0..N) with parallel_for and verify correctness.
## Task
Allocate vector, fill i, reduce with atomic or local+combine.
## Acceptance
- [ ] Sum equals N*(N-1)/2; passes repeatedly.