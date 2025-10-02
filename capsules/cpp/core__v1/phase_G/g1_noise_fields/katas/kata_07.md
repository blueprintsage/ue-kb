---
title: G1/k7 — SDF Primitives & Smooth Blends
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Implement SDFs (sphere, box, torus) and smooth boolean ops.
## Tasks
- Define primitives; implement smooth union/intersect/subtract (e.g., polynomial or exponential smooth min).  
- Provide normal via ∇d approximation; tiny raymarch demo.
## Acceptance
- [ ] Correct sign (inside<0, outside>0); blends C1‑smooth.  
- [ ] Raymarch renders without artifacts at sane step counts.