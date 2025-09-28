---
title: F2/k25 — Decisions Property Harness & Fuzz
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Fuzz and property‑test decision layers for determinism, budget adherence, and invariants.
## Task
Randomize stimuli/targets with fixed seed; assert: budget respected, replay deterministic, no deadlocks, no double‑claims, cooldowns honored.
## Acceptance
- [ ] 10k trials, zero invariant failures; worst‑case seeds logged.
- [ ] Budget overrun rate 0% with scheduler enabled.
## Keep/Revert
KEEP: seeded RNG + structured logs. REVERT: ad‑hoc tests with no reproducibility.