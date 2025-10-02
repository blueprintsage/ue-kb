---
title: A1/k3 — custom deleter injection
kit_id: a1_raii
version: 1.0
status: Draft
type: kata
---
## Goal
Allow external deleter strategy (callable) for the resource.
## Task
Pass a lambda/function to run on destruction.
## Acceptance
- [ ] Test confirms deleter invoked exactly once.