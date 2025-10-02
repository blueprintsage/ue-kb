---
title: F1/k11 — Path Following (Waypoints + Arrive per Segment)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Follow a loop/line of waypoints by seeking the closest point on the current segment and arriving at the segment end.
## Task
Project agent to segment i→i+1 to get target; if near end, advance to next; use Arrive near each waypoint.
## Acceptance
- [ ] Zero ping‑pong at corners (look‑ahead ≥ speed×t_look).
- [ ] Lap time stable across runs; no miss of any waypoint.