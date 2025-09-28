---
title: E1/k25 — ONB Stress: Randomized Property Test
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Property‑test your ONB builders (k4, k11): for random inputs, frames are orthonormal and right‑handed.
## Task
Generate 10k random normals/tangents; build frames; assert `R^T R≈I`, `det(R)>0`, and continuity (small input deltas → small frame deltas).
## Acceptance
- [ ] Max orthonormality error < 1e‑5; % failures = 0.
- [ ] No flips near poles beyond threshold.
## Keep/Revert
KEEP: continuous branch choices; epsilon guards. REVERT: discontinuous fallback that flips frames.