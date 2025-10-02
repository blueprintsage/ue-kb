---
title: F2/k7 — BT Parallel & Abort Policies
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Implement Parallel node (Or/And) and priority interrupts.
## Task
Run pursuit and avoidance in parallel; abort lower priority when hazard appears.
## Acceptance
- [ ] Or/And semantics pass truth-table tests.
- [ ] Preemption cancels running child cleanly.