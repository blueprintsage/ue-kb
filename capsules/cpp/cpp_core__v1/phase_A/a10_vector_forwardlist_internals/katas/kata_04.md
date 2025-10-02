---
title: A10/k4 — forward_list splice_after
kit_id: a10_vector_forwardlist
version: 1.0
status: Draft
type: kata
---
## Goal
Use `splice_after` to move a sublist between lists without allocations.
## Task
Create L1: [a,b,c,d], L2: [x,y]; splice [b,c] from L1 after x in L2; assert sequences.
## Acceptance
- [ ] Result L1 = [a,d], L2 = [x,b,c,y]; no allocations performed.