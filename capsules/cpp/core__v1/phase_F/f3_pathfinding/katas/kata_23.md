---
title: F3/k23 — Anytime Repairing A* (ARA*)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Produce a quick suboptimal path then improve it over time using **ARA*** (decreasing inflation w).
## Task
Start with w₀>1; run Weighted A*; then iteratively lower w and reuse `inconsistent`/open lists to improve path until w→1 or budget exhausted.
## Acceptance
- [ ] Each iteration’s path cost ≤ previous; converges to optimal as w→1.
- [ ] Time‑quality curve logged; meets real‑time budgets.