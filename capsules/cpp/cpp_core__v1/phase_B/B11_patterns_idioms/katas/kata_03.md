---
title: B11/k3 — Iterator invalidation (vector reallocation)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Show how push_back/reserve invalidate iterators and how to re-acquire safely.
## Acceptance
- [ ] Failing pre-fix test; post-fix reacquires iterators and passes; table of invalidating ops included.
