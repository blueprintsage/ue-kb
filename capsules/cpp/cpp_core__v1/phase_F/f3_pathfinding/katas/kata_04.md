---
title: F3/k4 — A* Implementation (Binary Heap Open Set)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement A* with binary‑heap priority queue and parent pointers.
## Task
Support tie‑breaking on equal f by greater g or smaller h; reconstruct path; count expansions.
## Acceptance
- [ ] Optimality under consistent heuristic; stable tie‑break reduces zig‑zag.
- [ ] Complexity O(E log V); no re‑insert leaks.