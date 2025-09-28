---
title: E4/k6 — Exponential Moving Average (Half-life)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Implement EMA with half-life parameterization for stable smoothing.
## Task
Given half-life H and dt, compute α = 1 - 2^(-dt/H); update y ← y + α(x - y).
## Acceptance
- [ ] Step response hits 50% at t≈H; stable for variable dt.
- [ ] Equivalent to continuous-time low-pass discretization.
## Keep/Revert
KEEP: derive α from half-life. REVERT: fixed α that breaks with variable dt.