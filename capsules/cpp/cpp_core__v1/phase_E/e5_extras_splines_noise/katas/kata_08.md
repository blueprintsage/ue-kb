---
title: E5/k8 — Tiled Noise (Period Wrap)
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Generate noise that tiles with a specified integer period P in both axes.
## Task
Wrap lattice coordinates with modulo P inside the permutation lookup; verify seamless borders.
## Acceptance
- [ ] Texture edges match within 1e-6; no seam when tiled.
- [ ] Period exactly P in x and y.
## Keep/Revert
KEEP: wrap inside hash, not on input domain. REVERT: fmod on x,y only (perm breaks).