---
title: F1/k8 — Perception: FOV, LOS & Memory Decay
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Detect targets via **field-of-view** cone and **line-of-sight** checks; store last seen with decay.
## Task
FOV via dot(th, forward) ≥ cos(θ/2); LOS via ray vs obstacles; memory timestamp and exponential decay.
## Acceptance
- [ ] Targets inside FOV+LOS become visible; outside or occluded fade.
- [ ] No stale targets after decay timeout.