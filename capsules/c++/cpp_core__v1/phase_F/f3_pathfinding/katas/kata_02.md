---
title: F3/k2 — Heuristics: Admissible & Consistent
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement Manhattan, Chebyshev, and Octile heuristics; prove/verify admissibility & consistency for chosen grid.
## Task
Unit tests check triangle inequality on edges; A* with each heuristic returns optimal path cost.
## Acceptance
- [ ] No overestimation; consistency holds on all edges.
- [ ] Nodes expanded ≤ Dijkstra for same maps.