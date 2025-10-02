---
title: F1/k13 — Containment (Stay Inside Arena/Polygon)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Keep agents inside a convex boundary using distance‑to‑edge forces.
## Task
Compute closest boundary distance; when < buffer, steer inward along inward normal proportional to penetration depth.
## Acceptance
- [ ] Zero boundary crossings in 5‑minute sim.
- [ ] Smooth re‑entry when spawned slightly outside.