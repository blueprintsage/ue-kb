---
title: E2/k21 — Recover LookAt Params From View Matrix
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Given a right‑handed view matrix `V`, recover `eye`, `forward`, `up` (a LookAt triple).
## Task
Compute `V^{-1}` to get world frame; `eye = (V^{-1} * (0,0,0,1)).xyz`. Recover basis from `V^{-1}` columns (right, up, forward). Normalize and verify.
## Acceptance
- [ ] Rebuilding `V' = LookAt(eye, eye+forward, up)` matches `V` within 1e‑6.
- [ ] Handles non‑uniform floating error (re‑orthonormalize basis).
## Keep/Revert
KEEP: normalize basis and fix handedness if det<0. REVERT: raw columns without normalization.