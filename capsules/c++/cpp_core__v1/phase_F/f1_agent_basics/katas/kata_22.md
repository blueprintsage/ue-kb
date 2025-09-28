---
title: F1/k22 — Potential Fields & Local Minima Escapes
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Navigate with attractive (goal) and repulsive (obstacle) potentials and add an escape strategy for local minima.
## Task
Compute F = −∇U where U = w_g‖x−g‖ + Σ w_o / (‖x−o‖+ε). Detect stall (‖F‖<δ, little progress) → switch to wall‑follow or random perturbation.
## Acceptance
- [ ] Reaches goal on mazes where pure potential gets stuck (≥95% trials).
- [ ] No orbiting near obstacles; escape triggers logged.
## Keep/Revert
KEEP: stall detector + escape mode. REVERT: pure gradient descent only.