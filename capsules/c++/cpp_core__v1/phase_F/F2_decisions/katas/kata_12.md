---
title: F2/k12 — Blackboard Derived Keys & Selectors
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Compute **derived keys** (e.g., distance_to_target, has_cover) lazily and cache with TTL; use them in BT conditions.
## Task
Register compute callbacks for derived keys; mark dirty sets on base key change; read‑through cache in BT conditions.
## Acceptance
- [ ] Derived keys recompute only when dependencies change.
- [ ] BT branches react within one tick of dependency updates.