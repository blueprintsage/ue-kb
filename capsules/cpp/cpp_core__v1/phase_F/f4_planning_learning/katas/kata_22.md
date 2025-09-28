---
title: F4/k22 — Plan Cache & Invalidation
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Reuse recent GOAP plans when goals/world barely change; **invalidate** safely on relevant fact changes.
## Task
Key cache by (goal mask, relevant facts hash). Track plan dependencies (facts touched). On change in deps → invalidate; else reuse with quick precheck.
## Acceptance
- [ ] ≥50% fewer replans on noisy but equivalent states.
- [ ] Zero stale‑plan executions (precheck blocks).
## Keep/Revert
KEEP: dependency set captured per plan. REVERT: cache keyed only by goal string.