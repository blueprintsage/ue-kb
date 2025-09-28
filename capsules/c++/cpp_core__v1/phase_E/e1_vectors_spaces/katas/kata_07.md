---
title: E1/k7 — Barycentric & Point‑In‑Triangle
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---

## Objective
Implement robust barycentric coordinates and a point‑in‑triangle test.

## Task
Compute (u,v,w) for P in ΔABC using area or projection method; point is inside if u,v,w∈[−ε,1+ε] and sum≈1.

## Acceptance
- [ ] Matches edge‑sign method across random tests.
- [ ] Boundary points classified as inside with ε=1e‑6.

## Keep/Revert
KEEP: epsilon slop on edges. REVERT: strict 0..1 causing boundary flicker.