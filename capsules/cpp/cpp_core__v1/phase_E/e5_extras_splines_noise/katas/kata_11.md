---
title: E5/k11 — Bezier Subdivision (de Casteljau Split)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Split a quadratic/cubic Bezier at parameter t into two Beziers with exact continuity.
## Task
Use de Casteljau to compute control points for left/right sub-curves at t=0.5 and arbitrary t; verify reconstruction.
## Acceptance
- [ ] Concatenate sub-curves reproduces original samples ≤1e-7.
- [ ] C0 continuity at split point; C1 when the original is C1.
## Keep/Revert
KEEP: compute all intermediate lerps. REVERT: cut the polyline (control polygon) directly.