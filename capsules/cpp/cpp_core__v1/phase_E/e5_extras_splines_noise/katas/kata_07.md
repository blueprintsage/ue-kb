---
title: E5/k7 — Fractal Brownian Motion (fBM)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Sum octaves of base noise with lacunarity and gain to generate richer spectra.
## Task
fBM(x)=Σ_{i=0}^{k-1} noise(λ^i x) * g^i; choose λ≈2, g≈0.5; normalize by Σ g^i.
## Acceptance
- [ ] Energy normalized (variance roughly constant across k).
- [ ] Increasing k adds detail without blowing range.
## Keep/Revert
KEEP: amplitude normalization. REVERT: omit normalization (range creep).