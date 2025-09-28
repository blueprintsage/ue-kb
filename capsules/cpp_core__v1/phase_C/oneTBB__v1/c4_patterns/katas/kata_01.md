---
title: C4/k1 — pipeline + limiter
kit_id: c4_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Build a 3‑stage pipeline with bounded in‑flight.
## Task
Use Flow Graph nodes; set `limiter_node(K)`; verify throughput and bounds.
## Acceptance
- [ ] Correct outputs; peak in‑flight = K.