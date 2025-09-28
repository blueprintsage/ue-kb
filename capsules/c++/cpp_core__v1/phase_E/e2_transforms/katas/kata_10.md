---
title: E2/k10 — Shortest‑Arc Rotation (Align a→b)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Compute quaternion that rotates unit vector a to unit vector b along the shortest arc.
## Task
If dot(a,b)≥1−ε → identity. If ≤−1+ε → pick orthogonal axis. Else axis = normalize(a×b); angle = acos(dot(a,b)); build quat.
## Acceptance
- [ ] q*a ≈ b within 1e‑6 for random tests.
- [ ] Stable for nearly opposite vectors with fallback axis.
## Keep/Revert
KEEP: guarded opposite case. REVERT: divide by zero from tiny cross.