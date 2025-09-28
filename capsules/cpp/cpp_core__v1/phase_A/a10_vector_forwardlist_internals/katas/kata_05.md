---
title: A10/k5 — reserve microbench
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Measure push_back cost with/without reserve for large N; show iteration cost differences vs forward_list.
## Task
Run timed loops for N = {1e3, 1e5, 1e6} and compare times for push + iterate.
## Acceptance
- [ ] Reserve avoids repeated reallocs; vector iteration beats forward_list for large N.