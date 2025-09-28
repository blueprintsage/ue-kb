---
title: E4/k24 — Denormals (FTZ/DAZ) & Tiny Epsilon Floors
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Observe performance/behavior impact of **denormal floats** and apply safe floors.
## Task
Microbench an inner loop with values near 1e−45..1e−38; enable/disable FTZ/DAZ (if platform API available) and/or clamp |x|<eps→0.
## Acceptance
- [ ] FTZ/DAZ or clamping removes slow path (timings logged).
- [ ] Numerical results unaffected beyond eps tolerance.
## Keep/Revert
KEEP: documented platform toggle or manual floor. REVERT: let denormals thrash perf.