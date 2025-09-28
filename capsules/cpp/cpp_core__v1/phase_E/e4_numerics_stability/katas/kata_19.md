---
title: E4/k19 — Robust Root Finding: Bisection vs Newton
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Contrast guaranteed convergence (bisection) with fast but fragile (Newton).
## Task
Find root of f(x)=x^3−x−1 from different starts; use bisection on a bracketing interval and Newton from guesses; hybridize: Newton with bisection fallback.
## Acceptance
- [ ] Newton converges fast when derivative sane; hybrid always converges.
- [ ] Bisection satisfies tolerance in bounded iterations.
## Keep/Revert
KEEP: bracket check; derivative guard. REVERT: unconstrained Newton.