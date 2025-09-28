---
title: E3/k17 — Plane–AABB Classification
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Classify an AABB against a plane (front/back/intersect) using p-vertex/n-vertex trick.
## Task
Given plane (n,d), compute extreme points p/n; use signed distances to decide.
## Acceptance
- [ ] Agrees with vertex brute-force classification.
- [ ] Handles flipped normal consistently.
## Keep/Revert
KEEP: p/n vertex method. REVERT: test center only.