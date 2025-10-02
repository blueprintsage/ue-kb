---
title: B6/k9 — Contract macros (debug/release policy)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Create `EXPECTS`/`ENSURES` macros that assert in debug and log/fail-fast in release (configurable).
## Acceptance
- [ ] Behavior toggles by build flag; messages include file:line and expression text.
