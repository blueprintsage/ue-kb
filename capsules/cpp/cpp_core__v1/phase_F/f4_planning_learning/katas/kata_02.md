---
title: F4/k2 — Action Spec (Preconditions, Effects, Cost)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Represent actions with masks and a callable cost function (time/energy/risk).
## Task
`struct Action { mask onReq, offReq, onEff, offEff; float cost(const State&); }` Validate applicability and apply effects to clone state.
## Acceptance
- [ ] Applicability/effects unit‑tested; costs non‑negative.
- [ ] Serialization round‑trips (domain files).