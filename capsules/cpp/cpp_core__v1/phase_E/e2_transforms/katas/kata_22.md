---
title: E2/k22 — Dual Quaternions for Rigid Transforms
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Represent a rigid transform (R,t) as a **unit dual quaternion**, apply it to points, and show equivalence to matrix form.
## Task
Build `qd = (qr, qd)` with `qr` unit rotation, `qd = 0.5 * (0, t) * qr`. Normalize dual quaternion; transform point p using dq·(0,p)·dq⁻¹.
## Acceptance
- [ ] For random rigid transforms, dq transform equals matrix transform within 1e‑6.
- [ ] Composition with dual quats matches matrix composition.
## Keep/Revert
KEEP: renormalize `qr` each step; unit dual check. REVERT: skip normalization → drift.