---
title: E5/k14 — Rational Quadratic (NURBS) Circle Arc
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Construct a rational quadratic curve that exactly represents a circular arc.
## Task
Derive control points and weights for a 90° arc; sample and compute max radial error.
## Acceptance
- [ ] Max |‖p(t)‖−R| ≤ 1e-6 for unit circle.
- [ ] Weights positive; endpoints on the circle.
## Keep/Revert
KEEP: use w=√2/2 at the middle. REVERT: approximate circle with polynomial Bezier.