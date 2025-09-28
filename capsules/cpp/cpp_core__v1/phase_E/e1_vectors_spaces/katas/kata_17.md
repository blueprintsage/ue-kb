---
title: E1/k17 — Construct TBN Frame From Normal & Tangent
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Build Tangent‑Bitangent‑Normal frame suitable for shading/geometric transforms.
## Task
Given normal n and surface tangent t (non‑parallel), orthonormalize t against n, set b = cross(n,t).
## Acceptance
- [ ] {t,b,n} orthonormal; det(R)=+1 (right‑handed).
- [ ] Stable when t≈n (fallback tangent).
## Keep/Revert
KEEP: reproject t, right‑handed check. REVERT: cross order that yields left‑handed frame.