---
title: E2/k17 — AABB Frustum Culling
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Cull axis‑aligned boxes against frustum planes using the p‑vertex/n‑vertex trick.
## Task
Implement test(Box,Planes) returning Out/Intersect/In; unit test with moving camera.
## Acceptance
- [ ] No false negatives; minimal false positives.
- [ ] Stable near plane boundaries.
## Keep/Revert
KEEP: p/n vertex per plane. REVERT: test center only.