---
title: E1/k12 — Uniform Random Unit Vectors
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Generate **uniform** directions on S² (no pole bias) using Marsaglia or normal‑dist sampling.
## Task
Implement two methods; run chi‑square or KS test on polar angle distribution.
## Acceptance
- [ ] Histogram of cosθ is ~uniform (p>0.05 on test).
- [ ] Methods agree within statistical variance.
## Keep/Revert
KEEP: sample z∈[−1,1], φ∈[0,2π). REVERT: θ uniform in [0,π] (polar bias).