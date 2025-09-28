---
title: E5/k18 — Simplex Noise 2D
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **2D Simplex noise** (skewed grid) and compare cost/quality to Perlin.
## Task
Follow skew/unskew transform; pick simplex corners; weight by radial kernel; hash gradients.
## Acceptance
- [ ] Visuals lack grid artifacts; roughly 30–40% fewer ops than Perlin.
- [ ] Range and variance comparable (after normalization).
## Keep/Revert
KEEP: correct skew/unskew constants. REVERT: treat as square lattice.