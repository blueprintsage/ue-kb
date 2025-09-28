---
title: F3/k22 — Bidirectional A*
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Search from **start** and **goal** simultaneously and meet in the middle for speed gains.
## Task
Run forward/backward A* with consistent heuristics; terminate when min(f_fwd)+min(f_bwd) ≥ best_path; stitch meeting point to form path.
## Acceptance
- [ ] Same optimal cost as single‑source A*.
- [ ] Expansion count significantly lower on long corridors/open maps.