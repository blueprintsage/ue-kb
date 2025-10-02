---
title: E4/k20 — RNG Determinism & Stratified Sampling
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Ensure reproducible randomness and lower-variance estimates.
## Task
Use `std::mt19937` with fixed seed; demonstrate identical sequences across runs; implement 1D stratified sampling and compare variance vs pure random on integral estimate.
## Acceptance
- [ ] Same seed → identical results; different seeds → different streams.
- [ ] Stratified estimator variance < naive by measured factor.
## Keep/Revert
KEEP: separate RNG instances per thread. REVERT: shared RNG without locking.