---
title: E5/k15 — Catmull–Rom ↔ Bezier Conversion
kit_id: e5_extras_splines_noise
version: 1.0
status: Draft
type: kata
---
## Objective
Convert a Catmull–Rom segment to an equivalent cubic Bezier (and back) for tool interchange.
## Task
Given p_{i-1},p_i,p_{i+1},p_{i+2} and tension τ, derive Bezier control points; validate round-trip.
## Acceptance
- [ ] Bezier and Catmull–Rom sample points agree ≤1e-5.
- [ ] Handles endpoint segments via endpoint duplication.
## Keep/Revert
KEEP: centripetal parameterization for stability. REVERT: uniform on uneven spacing.