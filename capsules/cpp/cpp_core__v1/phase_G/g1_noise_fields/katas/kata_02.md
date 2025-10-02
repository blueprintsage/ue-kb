---
title: G1/k2 — fBM & Normalization
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Sum octaves with lacunarity/gain; normalize amplitude and keep variance stable across octave counts.
## Tasks
- Implement `fbm(n, octaves, lacunarity, gain)` and compute exact max possible amplitude for normalization.  
- Provide tiling by using tiled base noise at all octaves (period multiples).  
- Add seed pass‑through and deterministic spectra.
## Acceptance
- [ ] Variance roughly constant as octaves↑; no clipping.  
- [ ] Tiling preserved; seeds reproduce bit‑stably.