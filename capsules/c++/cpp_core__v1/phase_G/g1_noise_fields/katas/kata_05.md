---
title: G1/k5 — Curl Noise (Divergence‑Free Field)
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Compute curl of a 3D potential field to produce divergence‑free velocity for flow.
## Tasks
- Use finite differences on three scalar noises to form vector potential; curl = ∇×A.  
- Validate ∇·(∇×A)=0 numerically; expose scale and time scroll.
## Acceptance
- [ ] Divergence ≈ 0 across samples; stable streamlines for small dt.  
- [ ] Deterministic under seed; no NaNs.