---
title: B10/k7 — Arena/region allocator & teardown in O(1)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a bump arena with mass free at scope end.
## Acceptance
- [ ] Objects allocated/freed correctly; teardown is O(1); fragmentation characteristics documented.
