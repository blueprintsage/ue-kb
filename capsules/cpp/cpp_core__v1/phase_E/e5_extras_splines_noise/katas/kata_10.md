---
title: E5/k10 — Smoothstep vs Lerp
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Compare plain linear interpolation to **smoothstep**/**smootherstep** easing for transitions.
## Task
Implement `smoothstep(t)=t^2(3−2t)` and `smootherstep(t)=t^3(10−15t+6t^2)`; compare endpoint slopes and overshoot; visualize ramp.
## Acceptance
- [ ] smoothstep has zero slope at t=0,1; no overshoot; monotone.
- [ ] Choose appropriate easing per use-case and document.
## Keep/Revert
KEEP: clamp t to [0,1] before easing. REVERT: un-clamped t causing non-monotone behavior.