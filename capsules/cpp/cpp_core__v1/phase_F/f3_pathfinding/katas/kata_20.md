---
title: F3/k20 — Path Executor: Arrive Along Path + Replan Hook
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Follow a path with Arrive (F1) and handle dynamic replans.
## Task
Consume waypoints; when blocked or target moves, trigger replan (LPA*/D*); log handoff times.
## Acceptance
- [ ] Zero collisions; smooth corners; replans under dynamics succeed.
- [ ] Latency within budget; executor never stalls on invalid path.