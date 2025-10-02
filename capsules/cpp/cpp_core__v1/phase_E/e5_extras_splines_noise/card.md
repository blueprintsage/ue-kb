---
title: E5 — Extras (Splines/Noise/Interpolation)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
category: Math
assets: []
dependencies: [e1_vectors_spaces, e2_transforms]
---

## Objective
Implement common curve/noise tools: Hermite/Catmull–Rom/Bezier, Perlin/FBM, domain warps, and interpolation tricks.

## Steps
1) Bezier eval (de Casteljau) and tangents.  
2) Cubic Hermite & Catmull–Rom; tension/bias.  
3) Arc‑length sampling (approx).  
4) Perlin noise 2D + FBM; tiling.  
5) Domain warp basics; combining noises.

## Smoke Test
- [ ] Curves interpolate endpoints; C1 continuity holds.  
- [ ] Noise value ranges and tiling constraints satisfied.

## Blueprint Hook
BP: Curve assets for tweens; noise textures/material params for procedural motion; Acceptance: smooth path & looped noise.