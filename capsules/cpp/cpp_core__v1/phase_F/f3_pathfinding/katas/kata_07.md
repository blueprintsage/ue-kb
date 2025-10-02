---
title: F3/k7 — Jump Point Search (JPS)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Accelerate grid A* with **JPS** by pruning symmetric neighbors and jumping to natural/forced neighbors.
## Task
Implement pruning rules; jump recursively along directions; compare expansions vs plain A*.
## Acceptance
- [ ] Same path cost as A*; ≥2× fewer expansions on open maps.
- [ ] Corner cases (corridors, mazes) still correct.