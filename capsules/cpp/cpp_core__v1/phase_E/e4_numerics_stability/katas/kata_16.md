---
title: E4/k16 — RK4 vs Semi-Implicit Euler (Energy)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Compare energy behavior on harmonic oscillator for RK4 and semi-implicit Euler.
## Task
Simulate x¨ + ω² x = 0; measure energy drift over many periods for fixed dt.
## Acceptance
- [ ] RK4 shows much lower drift than explicit; semi-implicit bounded.
- [ ] Report drift per period; plot or numeric log acceptable.
## Keep/Revert
KEEP: same dt/ω for fair comparison. REVERT: mix dt across methods.