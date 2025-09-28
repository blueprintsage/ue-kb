---
title: E4/k25 — Numerics Property Harness & Fuzz
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Fuzz-test numeric helpers (eq, lerp, roots, exp/log) and assert invariants.
## Task
Generate 100k random cases across ranges; assert symmetry, monotonicity, bounds; log min/max epsilons; run with sanitizers.
## Acceptance
- [ ] Zero assertion failures; reproducible via fixed seed.
- [ ] Report summarizes worst‑case deltas and triggers for unstable regions.
## Keep/Revert
KEEP: seeded RNG + per‑case logging. REVERT: non‑deterministic fuzz with no logs.