---
title: F3/k9 — LOS Smoothing (String‑Pull on Grid)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Post‑process A* path by removing intermediate waypoints using LOS checks (string‑pull).
## Task
Greedy skip: keep last kept node; advance as far as LOS holds; record reduced path.
## Acceptance
- [ ] Waypoint count decreases without increasing path cost for any‑angle.
- [ ] No collisions introduced; verified by LOS.