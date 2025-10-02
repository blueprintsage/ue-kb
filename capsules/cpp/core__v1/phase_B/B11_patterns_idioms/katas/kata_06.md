---
title: B11/k6 — Signed/unsigned mixups & underflow/overflow
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Trigger UB/logic bugs with signed/unsigned comparisons; fix with domain-appropriate types and checks.
## Acceptance
- [ ] UBSan or test detects bug; corrected types + bounds checks pass cleanly.
