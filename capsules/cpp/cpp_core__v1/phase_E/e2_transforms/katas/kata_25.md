---
title: E2/k25 — TRS Property Test (Round‑Trip & Inverses)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Stress‑test your TRS utilities across random inputs.
## Task
Generate random TRS (bounded scales). Check: `decompose(compose(TRS)) ≈ TRS`, `inv(inv(M))≈M`, and `M * M^{-1}≈I`. Include negative scale cases.
## Acceptance
- [ ] Max elementwise error < 1e‑5 across 10k trials.
- [ ] No failures under sanitizer; numeric guards hit only on pathological cases.
## Keep/Revert
KEEP: tolerate small eps; explicit det/handedness checks. REVERT: assume ideal inputs.