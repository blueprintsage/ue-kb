---
title: F1/k23 — Noise, Jitter & Tie‑Breakers (Stability)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Use small randomized tie‑breakers and dithered decisions to avoid symmetric deadlocks while keeping runs reproducible.
## Task
Introduce seeded micro‑noise to heading or to decision thresholds; ensure deterministic sequence via per‑agent RNG.
## Acceptance
- [ ] Head‑to‑head agents no longer deadlock at doorways.
- [ ] Replays with same seeds are bit‑stable.
## Keep/Revert
KEEP: per‑agent RNG, fixed seed. REVERT: global RNG (order‑dependent behavior).