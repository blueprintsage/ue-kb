---
<title: F3/k12 — Dynamic Obstacles & Replanning>
kit_id: f3_pathfinding
version: 1.0
status: Draft
type: kata
---
## Objective
Handle moving/appearing obstacles by partial replanning.
## Task
On obstacle updates, run a limited‑radius D* Lite‑style or LPA* incremental update; compare to full re‑A*.
## Acceptance
- [ ] Replan cost within 5% of fresh A*; fewer expansions.
- [ ] No stale paths after obstacle appears.