---
title: F2/k3 — FSM Core (States, Transitions, Guards)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a simple FSM engine with guard predicates and entry/exit actions.
## Task
Wire patrol→chase→search; guards based on blackboard (see F1 perception); log transitions.
## Acceptance
- [ ] No illegal transitions; guards respected; logs match design.
- [ ] Deterministic outcomes for fixed stimuli.