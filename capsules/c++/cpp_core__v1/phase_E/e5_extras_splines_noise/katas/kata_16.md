---
title: E5/k16 — Frenet Frame & Curvature/Torsion
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Compute tangent T, normal N, binormal B, curvature κ and torsion τ along a 3D curve.
## Task
Use numerical derivatives of p(t); T=normalize(p'), N=normalize(T'), B=T×N; κ=‖p'×p''‖/‖p'‖^3.
## Acceptance
- [ ] Frames orthonormal within 1e-5; κ positive; τ finite where defined.
- [ ] Stable except at inflection points (document handling).
## Keep/Revert
KEEP: central differences, arc-length reparameterization optional. REVERT: forward diff with large h.