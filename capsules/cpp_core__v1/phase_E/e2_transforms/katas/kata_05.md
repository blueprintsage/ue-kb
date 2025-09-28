---
title: E2/k5 — Perspective Projection Matrix
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Build a perspective matrix (right‑handed, D3D‑style or GL‑style—pick one and document it) and test NDC mapping.
## Task
Given fovY, aspect, near, far, build P. Verify clip→NDC maps frustum corners to (±1,±1, zNDC).
## Acceptance
- [ ] Known corners land at expected NDC positions.
- [ ] Handled infinite far case if implemented.
## Keep/Revert
KEEP: consistent convention notes (RH/LH, depth range). REVERT: mixing conventions.