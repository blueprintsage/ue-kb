---
title: F3/k24 — Multi‑Criteria Costs (Risk + Distance)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Plan with **two costs**: distance and risk (danger map). Explore scalarization and Pareto tradeoffs.
## Task
Implement weighted sum cost C=α·dist+(1−α)·risk; sweep α∈[0,1]. Optionally compute Pareto frontier via label‑setting with dominance checks.
## Acceptance
- [ ] α sweep shows expected tradeoff; extreme α match pure distance/risk.
- [ ] Pareto set is minimal (no dominated labels); executor follows chosen policy.