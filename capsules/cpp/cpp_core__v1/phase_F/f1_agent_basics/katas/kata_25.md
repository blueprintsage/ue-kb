---
title: F1/k25 — Agent Basics Property Harness
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Property‑test F1 behaviors (seek/arrive/avoid/flock) for invariants and determinism.
## Task
Randomize scenes with seeded RNG; assert: speed ≤ maxSpeed+ε; separation distance ≥ d_min; identical seeds → identical logs; energy bounded with zero input.
## Acceptance
- [ ] 10k trials, zero invariant failures; worst‑case deltas logged.
- [ ] Replay reproduces trajectories within float epsilon.
## Keep/Revert
KEEP: fixed seeds + explicit invariants. REVERT: ad‑hoc manual spot checks.