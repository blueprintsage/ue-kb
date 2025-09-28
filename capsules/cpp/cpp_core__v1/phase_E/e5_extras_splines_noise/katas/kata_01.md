---
title: E5/k1 — Bezier Eval (de Casteljau)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Evaluate quadratic and cubic Bezier curves using **de Casteljau** (stable, geometric).
## Task
Implement de Casteljau for n=3,4 control points; sample t∈[0,1] on a grid; compare to polynomial form.
## Acceptance
- [ ] Values match naive polynomial within 1e-7 for well-scaled points.
- [ ] Endpoints exact, curve lies inside control polygon (convex hull).
## Keep/Revert
KEEP: iterative lerps; numerically stable. REVERT: Horner polynomial only for all t.