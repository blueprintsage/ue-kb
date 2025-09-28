---
title: F3/k19 — Funnel Algorithm (String‑Pull on Portals)
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Implement the classic **funnel** to smooth corridor paths.
## Task
Maintain left/right “apex” funnel; advance through portals; emit waypoints when funnel flips side.
## Acceptance
- [ ] Path shorter/equal to unsmoothed; remains inside corridor.
- [ ] Handles skinny portals without oscillation.