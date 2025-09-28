---
title: E2/k11 — Orthonormalize 3×3 (Gram–Schmidt)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Given a 3×3 basis with small drift, orthonormalize it.
## Task
Apply modified Gram–Schmidt to columns; ensure det>0 (flip as needed).
## Acceptance
- [ ] R^T R ≈ I within 1e‑6; det(R)=+1.
- [ ] Angle drift reduced vs input.
## Keep/Revert
KEEP: reproject second/third columns; re‑normalize each step. REVERT: naive normalize only.