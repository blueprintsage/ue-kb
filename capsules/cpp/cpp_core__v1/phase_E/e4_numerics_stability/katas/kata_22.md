---
title: E4/k22 — Horner’s Method (Polynomial Eval)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Evaluate polynomials with reduced operations and better stability using **Horner’s rule**.
## Task
Compare naive Σ a_k x^k vs Horner on random coefficients; report max relative error across x∈[−10,10].
## Acceptance
- [ ] Horner matches long-double reference within tighter bounds than naive.
- [ ] Operation count reduced; profile shows fewer muls.
## Keep/Revert
KEEP: Horner nested form. REVERT: repeated pow(x,k) sums.