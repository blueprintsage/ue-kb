---
title: F2/k16 — Utility Curves: Library & Normalization
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Provide a curve library (linear, power, logistic, piecewise) with inputs normalized and clamped.
## Task
Implement curve funcs with unit tests; ensure monotone mapping from feature→score; support inversion and bias.
## Acceptance
- [ ] Curves pass golden tests; no NaN/Inf; outputs ∈ [0,1].
- [ ] Changing bias shifts action choice as expected.