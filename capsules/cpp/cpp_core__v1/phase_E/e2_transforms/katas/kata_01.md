---
title: E2/k1 — Compose & Decompose TRS
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Compose a transform from Translation, Rotation (quaternion), and non‑uniform Scale, then recover TRS from the matrix.
## Task
Build M = T * R * S. Decompose M back to (T,R,S) and compare to inputs.
## Acceptance
- [ ] Recovered T within 1e‑6; R matches up to sign (q ≈ ±q0); S within 1e‑6.
- [ ] Recompose from decomposed TRS yields M within 1e‑6.
## Keep/Revert
KEEP: orthonormalize rotation before extraction. REVERT: read R from scaled columns without normalization.