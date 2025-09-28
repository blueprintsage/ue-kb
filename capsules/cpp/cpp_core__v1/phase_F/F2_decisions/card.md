---
title: F2 — Decisions (FSM, BT, Utility)
kit_id: f2_decisions
version: 1.0
status: Draft
category: AI
assets: []
dependencies: [f1_agent_basics]
---

## Objective
Stand up three decision systems—**FSM**, **Behavior Tree**, and **Utility AI**—sharing a common blackboard and tick budget, with deterministic replay.

## Steps
1) **Blackboard:** typed keys, timestamps, validity windows, and observers.
2) **FSM:** hierarchical states with guards, cooldowns, and entry/exit actions.
3) **BT:** Sequence/Selector/Parallel, services, decorators (cooldown, inverter, time limit), abort policies.
4) **Utility:** actions with considerations, response curves, normalization, hysteresis.
5) **Budget & Replay:** time-sliced evaluation; seeded RNG for tie-breakers; minimal replay log.

## Smoke Test
- [ ] Same scenario solved by all three frameworks; decisions align within tolerance.
- [ ] Replay reproduces decisions and timings bit-stably.

## Blueprint Hook (TL;DR)
**Transfers:** UE5 Blackboard/BT: use built-in **Selector/Sequence**, Decorators (Cooldown, Distance), Services (Sense poll).
**Mini demo:** BT patrol→chase with distance/cooldown decorators; a Utility task toggles flee vs fight via curve score.