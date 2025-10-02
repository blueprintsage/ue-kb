---
title: E5/k4 — Catmull–Rom: Uniform vs Centripetal
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Compare **uniform** and **centripetal** Catmull–Rom parameterizations to avoid loops/overshoot.
## Task
Given p_{i-1},p_i,p_{i+1},p_{i+2}, compute tangents with t-spacing: uniform (t_k=k), centripetal (Δt_k=‖p_k−p_{k-1}‖^{1/2}). Sample segment i→i+1.
## Acceptance
- [ ] Centripetal form reduces overshoot on unevenly spaced points.
- [ ] End conditions handled (use one-sided tangents or duplicate endpoints).
## Keep/Revert
KEEP: centripetal Δt^{1/2}. REVERT: uniform only on non-uniform data.