---
title: B10/k16 — Handle validity & null-state APIs
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Design explicit “empty/null” states with queries (`valid()`) and safe operations.
## Acceptance
- [ ] Operations on invalid handle are no-ops or return error; tests cover transitions valid↔invalid.
