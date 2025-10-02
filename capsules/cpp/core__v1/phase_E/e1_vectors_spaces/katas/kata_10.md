---
title: E1/k10 — Safe Normalize & Clamp
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Write a safe normalize that avoids division by ~0 and a saturating clamp.

## Task
Implement `normalize_eps(v, eps)` returning `v/‖v‖` if ‖v‖>eps else (0,0,0) and `saturate(x)` to [0,1].

## Acceptance
- [ ] No NaNs on zero vector.
- [ ] Matches unit outputs for typical inputs within 1e‑7.

## Keep/Revert
KEEP: early‑out on small norms. REVERT: blind division by norm.