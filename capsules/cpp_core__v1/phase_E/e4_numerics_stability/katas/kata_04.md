---
title: E4/k4 — Stable Quadratic Roots
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Compute quadratic roots with minimal cancellation.
## Task
Given ax²+bx+c=0, use `q = -0.5*(b + sign(b)*sqrt(b²-4ac))`; roots: `x1=q/a`, `x2=c/q`.
## Acceptance
- [ ] Matches reference roots across ill-conditioned cases (b²≈4ac).
- [ ] No catastrophic cancellation for near-equal roots.
## Keep/Revert
KEEP: use q and reciprocal second root. REVERT: direct `(-b±√Δ)/(2a)` for both.