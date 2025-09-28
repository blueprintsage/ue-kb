---
title: G1/k6 — Worley (Cell) Noise with Tiling
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Generate F1/F2 distances with wrapped point sets so the texture tiles.
## Tasks
- Jitter feature points per cell with seeded RNG; compute nearest two distances using 3×3 (2D) / 3³ (3D) neighbor cells; wrap indices by **P**.
## Acceptance
- [ ] Cellular patterns match references; no seams at tile boundaries.  
- [ ] Optional crack/ridge transforms validated.