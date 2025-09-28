---
title: E1/k23 — Spherical ↔ Cartesian (az/el)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Convert between spherical angles (azimuth φ, elevation θ) and unit Cartesian vectors.
## Task
Implement `dir(φ,θ) = (cosθ cosφ, cosθ sinφ, sinθ)` and inverse using `atan2`/`asin`; test round‑trip.
## Acceptance
- [ ] Round‑trip error < 1e‑6 across random angles.
- [ ] Handles wraparound at ±π and clamps at poles.
## Keep/Revert
KEEP: use `atan2(y,x)` for φ; clamp `sinθ` to [−1,1]. REVERT: naive `acos` losing sign.