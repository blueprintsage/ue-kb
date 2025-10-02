---
title: F1/k15 — Queueing at Bottlenecks (Anticipatory Brake)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Prevent pile‑ups at doors by braking when a leader’s projected stop overlaps yours.
## Task
Estimate stopping distance d=v²/(2a_max); if leader ray hit within d+gap, reduce desired speed with PID‑like term.
## Acceptance
- [ ] No overlaps at doorway; average throughput within 5% of optimal.
- [ ] Stable spacing without oscillation.