---
title: F2/k1 — Decision Tick Ordering & Budget
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Define a deterministic per-frame order: sense→blackboard update→decide→act; enforce a CPU budget.
## Task
Implement a scheduler that spreads BT/utility updates over frames and records timing.
## Acceptance
- [ ] Frame time ≤ budget; decisions repeat with same seeds.
- [ ] No starvation: each agent updated within ≤N frames.