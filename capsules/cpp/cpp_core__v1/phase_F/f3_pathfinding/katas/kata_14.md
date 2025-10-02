---
title: F3/k14 — D* Lite (Any‑time Replanning)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **D* Lite** over LPA* for agent‑moving‑toward‑goal replans.
## Task
Update start position each step; repair path on edge changes; compare to LPA*.
## Acceptance
- [ ] Same path quality as A*; fewer updates when start moves.
- [ ] Handles appearing obstacles while en route.