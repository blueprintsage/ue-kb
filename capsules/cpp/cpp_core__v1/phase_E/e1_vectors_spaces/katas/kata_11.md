---
title: E1/k11 — Fast Orthonormal Basis (Frisvad)
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Build an ONB from a unit normal using the **Frisvad** method (branchless, robust).
## Task
Given unit n, compute tangent/bitangent without branching; verify ONB.
## Acceptance
- [ ] ‖t‖≈‖b‖≈1 and {t,b,n} orthonormal within 1e‑6.
- [ ] Works for n≈(0,0,±1) without instability.
## Keep/Revert
KEEP: Frisvad closed form. REVERT: arbitrary fallback that flips at poles.