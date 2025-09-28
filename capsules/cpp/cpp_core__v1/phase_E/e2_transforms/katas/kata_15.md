---
title: E2/k15 — Decompose Affine With Negative Scale
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Robustly decompose M into TRS even when one or more scales are negative.
## Task
Use polar decomposition for R; extract S on diagonal; if det(R)<0, flip one axis and negate its scale.
## Acceptance
- [ ] Recompose equals M within 1e‑5 for random tests including negatives.
- [ ] Rotation remains right‑handed.
## Keep/Revert
KEEP: det check + axis flip. REVERT: lose sign in scales.