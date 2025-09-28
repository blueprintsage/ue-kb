---
title: F4/k7 — Partial‑Order Effects & Concurrency
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Allow independent actions to reorder/overlap safely.
## Task
Detect effect/requirement independence (no conflicting facts/resources); schedule non‑conflicting actions concurrently.
## Acceptance
- [ ] Throughput improves vs strict sequence; no races.
- [ ] Conflicts detected and serialized deterministically.