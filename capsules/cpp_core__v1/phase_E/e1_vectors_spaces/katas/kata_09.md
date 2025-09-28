---
title: E1/k9 — Refraction (Snell, clamped)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Compute refracted vector using Snell’s law with TIR guard.

## Task
Given incident `i` (unit), normal `n` (unit), eta = n1/n2, compute `t` or detect total internal reflection.

## Acceptance
- [ ] For non‑TIR cases, `‖t‖≈1` and energy direction correct.
- [ ] TIR path triggers flag and returns safe fallback.

## Keep/Revert
KEEP: `k = 1 − η^2(1 − c^2)` clamp. REVERT: negative sqrt without guard.