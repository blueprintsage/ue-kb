---
title: G1/k3 — Ridged Multifractal
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Build ridged variant `r=1−|n|` with per‑octave weighting and post‑normalization.
## Tasks
- Compute ridge = (1−|n|); square to sharpen; accumulate with gain; renormalize to [0,1].  
- Provide contrast/bias knobs; preserve tiling.
## Acceptance
- [ ] Sharp ridges, no plateau clipping; histogram within [0,1].  
- [ ] Stable under frequency/seed sweeps.