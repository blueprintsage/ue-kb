---
title: E5/k2 — Bezier Tangent & Curvature
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Compute first derivative (tangent) and approximate curvature κ on cubic Bezier.
## Task
Analytic derivative via control-point differences; validate vs central finite-difference derivative; compute curvature κ=|x'y''−y'x''|/(x'^2+y'^2)^{3/2} (2D case).
## Acceptance
- [ ] Tangent angle error < 1e-6 rad vs finite diff (moderate step h).
- [ ] Curvature finite and continuous on (0,1); endpoints handle safely.
## Keep/Revert
KEEP: clamp t away from 0/1 for numeric second derivative. REVERT: naive h causing noise.