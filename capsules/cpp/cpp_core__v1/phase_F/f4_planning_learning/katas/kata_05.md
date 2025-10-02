---
title: F4/k5 — Resources, Cooldowns & Mutex Facts
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Augment GOAP with numeric resources (ammo, stamina) and mutual‑exclusion predicates.
## Task
Extend state with small ints; preconditions check resource thresholds; effects change resources; enforce mutex sets.
## Acceptance
- [ ] Plans respect resources; no negative values; mutex never violated.
- [ ] Planner prunes impossible branches early.