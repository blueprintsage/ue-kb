---
title: E2/k16 — Frustum Planes From VP
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Extract 6 frustum planes (L,R,B,T,N,F) from a View‑Projection matrix.
## Task
Read rows of VP; form planes; normalize (n,d). Validate against known points.
## Acceptance
- [ ] Unit normals; points on/inside return ≥0 signed distance.
- [ ] Matches hand‑computed planes for a simple camera.
## Keep/Revert
KEEP: consistent RH/LH convention. REVERT: mix GL/D3D depth ranges.