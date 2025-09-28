---
title: F3/k10 — Heuristic & Tie‑Break Ablation Study
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Measure impact of heuristic choice and tie‑breaking on expansions and path quality.
## Task
Sweep (Manhattan/Chebyshev/Octile) × (g‑favored/h‑favored) × (turn‑penalty on/off) on random maps.
## Acceptance
- [ ] Report table of expansions, cost, turns; pick a default policy.
- [ ] Selected policy yields best trade‑off on median case.