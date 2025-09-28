---
title: BR17 — Procedural Generation Basics (BP)
kit_id: br17_procgen
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR17_ProcGen_Map
media:
- type: screenshot
views: [TOP, BEAUTY]
assets: []
dependencies: []
---


## Objective
Scatter actors on a grid with a seed for reproducibility; avoid overlaps with simple checks.


## Steps
1) Seed RNG; generate grid points within bounds.
2) Randomly cull points by density; test surface via line trace.
3) Spawn actors at valid points with random yaw/scale range.


## Acceptance
- [ ] Re-running with same seed reproduces layout.
- [ ] No overlapping spawns beyond tolerance.