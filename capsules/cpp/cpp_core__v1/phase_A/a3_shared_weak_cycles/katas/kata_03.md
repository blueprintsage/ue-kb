---
title: A3/k3 — aliasing constructor
kit_id: a3_shared_weak_cycles
version: 1.0
status: Draft
type: kata
---
## Goal
Use `shared_ptr<T>(owner, owner->member)` to keep member alive via owner's control block.
## Task
Create `shared_ptr<Owner> o = make_shared<Owner>(); shared_ptr<Member> m(o, &o->member);`
## Acceptance
- [ ] Access to `m` stays valid as long as `o` remains; UB avoided.