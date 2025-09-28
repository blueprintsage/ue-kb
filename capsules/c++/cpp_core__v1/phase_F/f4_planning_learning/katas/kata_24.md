---
title: F4/k24 — Safety & Ethical Constraints in Planning
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Enforce **hard constraints** (never do X) and **soft constraints** (prefer Y) across GOAP/BT/Utility.
## Task
Hard: filter action set by allowlist/denylist tags before search. Soft: penalty added to cost/utility. Provide audit log of rejected actions.
## Acceptance
- [ ] No plan contains denied actions; logs show enforcement points.
- [ ] Soft constraints steer choices without dead‑ending.
## Keep/Revert
KEEP: single source of truth for constraints. REVERT: scattered checks across subsystems.