---
title: A2/k1 — function‑ptr vs functor deleter
kit_id: a2_unique_ptr_deleters
version: 1.0
status: Draft
type: kata
---
## Goal
Create `unique_ptr` with (a) function‑pointer deleter and (b) functor deleter; compare type and default constructibility.
## Task
Implement both forms for `FILE*` (or dummy handle); static_assert they are different types; ensure both compile and close exactly once.
## Acceptance
- [ ] Tests confirm single close; types differ as expected.