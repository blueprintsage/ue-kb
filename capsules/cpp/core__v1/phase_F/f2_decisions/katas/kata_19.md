---
title: F2/k19 — Decision Debugging: Trace & Heatmaps
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Generate per‑frame **decision traces** and optional heatmaps of scores/conditions for visualization.
## Task
Emit compact logs (node id, status, duration, scores). Aggregate into a CSV/JSON; render simple heatmap of scores over time.
## Acceptance
- [ ] Trace explains all transitions; no missing ticks.
- [ ] Heatmap reveals thrash which drops after hysteresis enabled.