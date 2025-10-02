---
title: F4/k4 — Heuristics for GOAP (Goal Distance)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Design admissible heuristic: count of unsatisfied sub‑goals or weighted sum.
## Task
`h(s)=Σ w_i * [goal_i unmet]` or relaxed planning graph (delete‑relaxation) approximation (lightweight).
## Acceptance
- [ ] Heuristic never overestimates; expansions less than h=0.
- [ ] Weighted variant remains admissible when weights ≤ min action cost to satisfy goal.