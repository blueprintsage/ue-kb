---
title: E5/k21 — Kochanek–Bartels (Tension/Bias/Continuity)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **Kochanek–Bartels** (T/B/C) cubic splines and study how parameters affect shape and continuity.
## Task
Given four points p_{i-1..i+2} and params T,B,C∈[−1,1], compute incoming/outgoing tangents at p_i; evaluate segment i→i+1.
## Acceptance
- [ ] T=0,B=0,C=0 equals Catmull–Rom.
- [ ] Increasing T tightens curve; ±B skews; ±C shifts ease-in/out (visually and numerically).
- [ ] C1 continuity across interior knots.
## Keep/Revert
KEEP: derive tangents per KB formulas; clamp extremes. REVERT: reuse Catmull–Rom regardless of T/B/C.