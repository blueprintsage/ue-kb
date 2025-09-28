---
title: F4/k19 — Non‑Stationary Bandits (Discount/Window)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Adapt to drifting reward distributions using **exponential discounting** or **sliding windows**.
## Task
Maintain EMA estimates with half‑life H or keep last W samples; compare regret under piecewise‑stationary sequences.
## Acceptance
- [ ] Discount/window variants recover after change points faster than stationary methods.
- [ ] Tuned H/W balances adaptivity vs noise (sweep study recorded).