---
title: E5/k24 — Ridged/Turbulence Noise Variants
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Build **ridged multifractal** and **turbulence** from base noise to create sharper features.
## Task
Ridged: r = (1−|n|); accumulate octaves with gain/offset; Turbulence: sum |n_i| with decreasing amplitude. Normalize outputs to [0,1].
## Acceptance
- [ ] Histograms within [0,1]±1e−6 after normalization.
- [ ] Visuals show crisp ridges (ridged) and marbled patterns (turbulence).
## Keep/Revert
KEEP: per-octave amplitude normalization. REVERT: no normalization (range drift).