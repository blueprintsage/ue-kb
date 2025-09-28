---
title: E2/k6 — Orthographic Projection Matrix
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Build an orthographic projection matrix and validate mapping of a known box.
## Task
Given left,right,bottom,top,near,far, build O and test corners.
## Acceptance
- [ ] Box corners map to (±1,±1, zNDC) as expected.
- [ ] Depth direction consistent with chosen convention.
## Keep/Revert
KEEP: document near/far sign conventions. REVERT: swap near/far silently.