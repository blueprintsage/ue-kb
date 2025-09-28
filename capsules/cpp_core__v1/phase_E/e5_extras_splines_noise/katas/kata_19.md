---
title: E5/k19 — Poisson Disk (Bridson) Blue-Noise
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Generate 2D blue-noise points with minimal spacing r using **Bridson’s** algorithm.
## Task
Grid-accelerated dart throwing with k=30 candidate attempts; support bounded domain.
## Acceptance
- [ ] No pairs closer than r; radial distribution ~annular.
- [ ] Runtime near O(n); grid lookups reduce neighbors checks.
## Keep/Revert
KEEP: cell size r/√2; active list loop. REVERT: naive rejection sampling.