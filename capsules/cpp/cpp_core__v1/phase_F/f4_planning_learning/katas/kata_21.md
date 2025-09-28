---
title: F4/k21 — GOAP Domain Files (Compile & Validate)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Author actions/goals in JSON/YAML and **compile** into masks/resources with validation.
## Task
Schema: facts list, actions {requires_on/off, effects_on/off, cost expr}, goals. Build compiler that emits bitmask IDs, checks name typos, mutex facts, unreachable goals.
## Acceptance
- [ ] Bad refs/typos rejected with line/col; mutex violations flagged.
- [ ] Compiled domain reproduces hand‑built plans on sample tests.
## Keep/Revert
KEEP: explicit fact registry + deterministic ID map. REVERT: ad‑hoc parsing with silent fallthroughs.