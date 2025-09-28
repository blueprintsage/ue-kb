---
title: F4/k11 — MCTS Transposition Table (Zobrist Hash)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Share statistics across identical states reached by different paths using a **transposition table**.
## Task
Implement Zobrist hashing (xor of feature keys) for domain states; store {N, W, Q} per state; update during backprop; avoid double-count in same trajectory.
## Acceptance
- [ ] Win‑rate/Q estimates converge faster vs no‑TT baseline.
- [ ] Hash collisions rare (logged) and handled (bucket or verify state).