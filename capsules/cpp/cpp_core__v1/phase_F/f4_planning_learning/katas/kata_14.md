---
title: F4/k14 — Value Backup Variants & Discounting
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Experiment with **backup rules**: mean, max, and discounted returns for non‑episodic tasks.
## Task
Implement backprop with γ∈(0,1]; compare mean‑backup vs max‑backup on stochastic domains; ensure numerical stability.
## Acceptance
- [ ] Discounted returns stabilize long‑horizon estimates.
- [ ] Max‑backup improves worst‑case policies where appropriate without biasing all domains.