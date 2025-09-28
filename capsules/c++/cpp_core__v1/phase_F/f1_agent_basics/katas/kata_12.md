---
title: F1/k12 — Wall Following (Surface Normal Deflection)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Skim along walls by deflecting desired velocity off contact normals.
## Task
On forward ray hit at distance<d, remove normal component from desired vel and renormalize; blend with goal seek.
## Acceptance
- [ ] Slides past convex corners without snagging.
- [ ] No oscillation when parallel to a long wall (add small tangent bias).