---
title: F3/k11 — Grid Raycast (Bresenham / Amanatides–Woo)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement grid‑aligned ray marching to test LOS and cost along rays.
## Task
Provide Bresenham (2D) and Amanatides–Woo (DDA) variants; return first blocked cell and traveled cost.
## Acceptance
- [ ] LOS matches reference; step counts plausible; no infinite loops at boundaries.
- [ ] Works with non‑uniform cell costs.