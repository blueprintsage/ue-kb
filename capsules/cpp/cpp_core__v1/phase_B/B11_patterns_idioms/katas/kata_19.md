---
title: B11/k19 — Template deduction surprises (CTAD, decay)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show deduction that drops refs/cv or picks unexpected constructors; fix with guides/constraints.
## Acceptance
- [ ] `static_assert` probes fail pre-fix; with guides/concepts they pass and express intent.
