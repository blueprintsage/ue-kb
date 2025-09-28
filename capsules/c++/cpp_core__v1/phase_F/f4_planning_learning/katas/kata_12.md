---
title: F4/k12 — Progressive Widening (Large Branching)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Control child expansion when actions are numerous via **progressive widening**.
## Task
Allow K(N)=⌈c·N^α⌉ children at visit count N (0<α<1). Add children in score order from a policy prior; compare to full branching.
## Acceptance
- [ ] Better reward vs time on high‑branch domains.
- [ ] As N grows, tree approaches full branching (sanity check).