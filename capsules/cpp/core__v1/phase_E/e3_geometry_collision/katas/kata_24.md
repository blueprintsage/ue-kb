---
title: E3/k24 — Box–Box Contact Manifold (Clip Faces)
kit_id: e3_geometry_collision
version: 1.0
status: Draft
type: kata
---
## Objective
Generate a small set of contact points for intersecting OBBs using SAT results.
## Task
Pick reference/incident faces from min-penetration axis; clip incident polygon against reference side planes; keep deepest points (≤4).
## Acceptance
- [ ] Manifold stable under small motions; normals consistent.
- [ ] Sum of impulses resolves overlap in a simple solver test.
## Keep/Revert
KEEP: clip against side planes, bias depth ε. REVERT: single contact at center only.