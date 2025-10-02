---
title: B9/k5 — Once-only init (call_once) vs double-checked lock
kit_id: b9_concurrency
version: 1.0
status: Draft
type: kata
---
## Objective
Safely initialize a singleton without data races.
## Acceptance
- [ ] `std::call_once` version passes; naive DCL fails under sanitizer or litmus test.
