---
title: E5/k25 — Curves & Noise Property Harness
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Property-test spline/noise utilities for invariants, continuity, tiling, and numeric stability.
## Task
Randomize control points/params; assert: spline endpoints exact; Catmull–Rom reduces to linear on collinear points; tiled noise matches on edges; numeric ops remain finite; seeds reproduce results.
## Acceptance
- [ ] 10k randomized trials, zero assertion failures.
- [ ] Logs capture worst-case errors and seed for reproduction.
## Keep/Revert
KEEP: fixed seed + min/max epsilon logs. REVERT: ad‑hoc manual tests only.