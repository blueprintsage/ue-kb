---
title: B6/k23 — Failure injection & chaos probe (deterministic)
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Add a failure-injection hook that deterministically fails allocations/IO at chosen points.
## Acceptance
- [ ] Two tests: one passes with no failures, one triggers failure #N and reports clean recovery or correct error surface.
