---
title: E5/k23 — Worley (Voronoi) Noise 2D
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Implement 2D **Worley (cell)** noise (F1, F2 distances) with grid-accelerated neighbor search; compare look to Perlin/Simplex.
## Task
Place jittered feature points per integer cell; for query x, examine surrounding cells; return min/second-min distances and derived patterns.
## Acceptance
- [ ] Tiling variant supported by wrapping grid index.
- [ ] Visuals show typical cellular patterns (cracks, ridges) without alias seams.
## Keep/Revert
KEEP: check 3×3 neighborhood (or 5×5 for large jitter). REVERT: scan all points globally.