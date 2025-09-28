---
title: A12/k4 — default_resource guard
kit_id: a12_pmr_custom_resources
version: 1.0
status: Draft
type: kata
---
## Goal
Temporarily set default_resource within a scope.
## Task
Guard sets thread-local default to pool; on destruction restores prior.
## Acceptance
- [ ] pmr containers created in scope use the pool; outside revert.