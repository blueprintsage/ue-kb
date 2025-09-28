---
title: A3/k2 — break with weak_ptr
kit_id: a3_shared_weak_cycles
version: 1.0
status: Draft
type: kata
---
## Goal
Replace one `shared_ptr` with `weak_ptr` and verify clean teardown.
## Task
`Node{ shared_ptr<Node> strong; weak_ptr<Node> weak; }` or similar; `.lock()` when needed.
## Acceptance
- [ ] Destructors fire; no leaks under ASan.