---
title: B2/k25 — Crash‑only Logging (Durable)
kit_id: b2_fundamentals_II
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a minimal crash‑resistant log with periodic fsync and atomic rename on rotation.
## Acceptance
- [ ] Survives abrupt termination without truncation; indices recover.