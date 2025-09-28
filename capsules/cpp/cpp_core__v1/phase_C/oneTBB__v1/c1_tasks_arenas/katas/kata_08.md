---
title: C1/k8 — progress reporting
kit_id: c1_tasks_arenas
version: 1.0
status: Draft
type: kata
---
## Goal
Report progress from tasks safely to a shared counter.
## Task
Use `std::atomic<int>`; avoid false sharing with padding.
## Acceptance
- [ ] Final count equals work items; UI thread remains responsive in demo.