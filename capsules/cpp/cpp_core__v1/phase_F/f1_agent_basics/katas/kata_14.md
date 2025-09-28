---
title: F1/k14 — Spatial Hash Grid (Neighbor Queries)
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Accelerate neighborhood lookups for flocking/avoidance with a uniform grid.
## Task
Hash agents to cells sized ≥ neighborhood radius; query current + 8 neighbors; compare complexity vs O(N²).
## Acceptance
- [ ] Same neighbor sets as brute‑force; ≥5× faster at N≥500.
- [ ] Deterministic membership with fixed seed/order.