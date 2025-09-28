---
title: E4 — Numerics & Stability
kit_id: e4_numerics_stability
version: 1.0
status: Draft
category: Math
assets: []
dependencies: [e1_vectors_spaces, e2_transforms]
---

## Objective
Write numerically robust math: epsilons, conditioning, compensated sums, stable roots/interpolations, and basic integrators.

## Steps
1) Epsilon comparisons; relative vs absolute tolerance.  
2) Conditioning examples; scaling inputs.  
3) Kahan/Neumaier summation.  
4) Stable quadratic roots; discriminant guards.  
5) Integrators: explicit/sem‑implicit Euler; stability regions.

## Smoke Test
- [ ] Robust equality helpers pass edge cases.  
- [ ] Integrator remains stable for dt within bound.

## Blueprint Hook
BP: Avoid divide‑by‑zero; clamp dt; smooth with exponential moving average; Acceptance: no jitter at small dt.