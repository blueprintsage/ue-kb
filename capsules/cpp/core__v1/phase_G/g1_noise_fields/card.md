---
title: G1 — Noise & Fields
kit_id: g1_noise_fields
version: 1.0
status: Draft
category: PCG
assets: []
dependencies: []
---

## Objective
Build robust scalar/vector noise and signed distance fields (SDF) that tile, are deterministic under seeds, and are numerically stable for downstream use (textures, heightmaps, flow fields).

## Steps
1) **Base noise:** Perlin/Simplex 2D/3D with seeded permutation and optional tiling period **P**.  
2) **Spectral stacks:** fBM (lacunarity/gain), **ridged** multifractal (1−|n|), normalization.  
3) **Warping & vectors:** domain warp; generate **curl noise** (divergence‑free).  
4) **Cell noise:** Worley (F1/F2) with tiling.  
5) **SDF kit:** primitives (sphere, box, torus) + smooth union/subtract/intersect; basic raymarch harness.  
6) **Post:** histogram match (target CDF) and domain remaps (height/roughness/flow strength).

## Smoke Test
- [ ] Tiling: samples equal across period **P**; no seams.  
- [ ] Stats: large images have near‑zero mean, controlled variance; no NaNs/Infs across sweeps.  
- [ ] Curl: ∇·v ≈ 0; stable streamlines for small dt.  
- [ ] SDF: correct signed distances; smooth blends (C1) without artifacts.

## Notes
- Centralize RNG seeding; duplicate permutation tables to avoid mod 256 branches.  
- Prefer integer masking (`&255`) over `% 256`; clamp/normalize stacks to avoid clipping.  
- Keep small demo programs under `examples/` for quick visual checks.