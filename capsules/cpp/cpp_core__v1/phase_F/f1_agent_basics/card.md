---
title: F1 — Agent Basics (Sensors, Steering, State)
kit_id: f1_agent_basics
version: 1.0
status: Draft
category: AI
assets: []
dependencies: []
---

## Objective
Build a robust agent loop: sensing → decision → steering → integration, with numerically safe updates and minimal allocations.

## Steps
1) **Sense:** FOV cones, LOS ray tests, memory with decay/refresh.
2) **Decide:** simple FSM (patrol→chase→search) with cooldowns.
3) **Steer:** seek/arrive/flee/pursuit; combine via priority & weighting.
4) **Integrate:** clamp accel/vel; semi-implicit update; avoid tunneling.
5) **Stabilize:** time-slicing for expensive ops; deterministic seeding.

## Smoke Test
- [ ] Ten agents avoid obstacles, converge on targets, and never exceed max speed.
- [ ] FSM transitions logged and reproducible with fixed seed.

## Blueprint Hook (TL;DR)
**Transfers:** FOV via dot threshold; LOS via line trace; FSM via State or Behavior Tree; **Mini demo:** BP pawn with tick → sense (dot+trace) → set blackboard → Seek (Interp To) until Arrive; test with moving target.