---
title: E1/k13 — Vector Triple Identity
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Verify the identity `a×(b×c) = b(a·c) − c(a·b)` numerically.
## Task
Implement both sides; compare max norm error over random vectors.
## Acceptance
- [ ] Error < 1e‑6 for |a|,|b|,|c| ≤ 10.
- [ ] Degenerate cases (zeros/collinear) handled.
## Keep/Revert
KEEP: fused operations to reduce error. REVERT: separate temp products with avoidable drift.