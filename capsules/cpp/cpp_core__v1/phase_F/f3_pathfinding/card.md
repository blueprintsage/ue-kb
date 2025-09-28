---
title: F3 — Pathfinding (Grids, Graphs, A*, HPA*, Navmesh)
kit_id: f3_pathfinding
version: 1.0
status: Draft
category: AI
assets: []
dependencies: [f1_agent_basics, f2_decisions]
---

## Objective
Implement robust pathfinding from grids to navmesh: graph build → search → smoothing → hierarchy, with clear invariants and perf metrics.

## Steps
1) **Graphs:** grid (4/8‑conn) with costs; adjacency + heuristics.
2) **Search:** Dijkstra, A*, Weighted A*, JPS, Theta* any‑angle.
3) **Smoothing:** string‑pull (grid LOS), funnel (navmesh) later.
4) **Hierarchy:** HPA* clusters/portals; cache & replan.
5) **Runtime:** budgets, deterministic seeds, heatmaps for debug.

## Smoke Test
- [ ] A* optimal on admissible/consistent heuristics; parity with Dijkstra at h=0.
- [ ] JPS/Theta* reduce expansions while preserving optimality/sub‑optimality bounds.

## Blueprint Hook (TL;DR)
**Transfers:** Use **NavMeshBoundsVolume** with **Simple Move to Location** for baseline, then detour crowd for avoidance. **Mini demo:** spawn grid from texture → draw debug paths (line trace for LOS smoothing). BT task requests path, blackboard key stores points; pawn follows with Arrive.