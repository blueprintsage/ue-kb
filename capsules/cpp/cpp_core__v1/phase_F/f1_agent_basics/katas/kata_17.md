---
title: F1/k17 — Leader Following (Separation + Pursuit)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Follow a leader while avoiding tailgating via separation from neighbors.
## Task
Pursue leader with capped look‑ahead; add separation from agents in front arc; weight blend with priority safety.
## Acceptance
- [ ] No rear‑end overlaps; path tracks leader within envelope.
- [ ] Handles stop‑and‑go without ping‑pong.