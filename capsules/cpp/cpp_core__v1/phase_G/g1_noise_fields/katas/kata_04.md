---
title: G1/k4 — Domain Warp & Flow Noise
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Warp coordinates by low‑frequency vector noise (or curl) to enrich patterns without aliasing.
## Tasks
- Generate low‑freq vector field; sample base noise at `p + warpStrength * v(p)`.  
- Keep warp ≤ recommended bounds; support chained warps.
## Acceptance
- [ ] No seams/banding; continuity preserved.  
- [ ] Parameter sweep produces usable ranges; no fold‑over artifacts.