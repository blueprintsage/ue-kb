---
title: F3/k8 — Any‑Angle: Theta*
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **Theta*** to allow line‑of‑sight (LOS) shortcuts on grids.
## Task
When expanding, if LOS(parent(current), neighbor) → relax with parent’s g + dist; else standard A* relax.
## Acceptance
- [ ] Path cost ≤ A* (4/8‑conn) and ≥ straight‑line lower bound.
- [ ] LOS test is robust (Bresenham or grid ray) with no tunneling through walls.