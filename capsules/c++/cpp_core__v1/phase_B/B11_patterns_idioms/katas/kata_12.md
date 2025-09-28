---
title: B11/k12 — Exceptions in destructors & stack unwinding
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show why throwing in a destructor during stack unwinding is fatal; fix with `noexcept(true)` and error sinks.
## Acceptance
- [ ] Death test pre-fix; safe destructor behavior post-fix; doc of policy (log-and-suppress vs fail-fast).
