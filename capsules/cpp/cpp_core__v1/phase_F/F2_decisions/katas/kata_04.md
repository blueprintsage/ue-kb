---
title: F2/k4 — Hierarchical FSM (HFSM)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Add substates with default entry and shared transitions (superstate rules).
## Task
Implement chase.{line_of_sight,search_last_seen}; shared exit on lost target.
## Acceptance
- [ ] Entering parent routes to default child; transitions bubble correctly.
- [ ] No state leaks after rapid toggling.