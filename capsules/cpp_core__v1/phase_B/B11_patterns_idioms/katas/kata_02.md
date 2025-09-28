---
title: B11/k2 — Dangling views/iterators (string_view, ranges)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Cause `string_view`/view to outlive the source, then fix via owning storage or lifetime extension.
## Acceptance
- [ ] ASan/UBSan test fails for dangling case; fixed version passes and documents rule.
