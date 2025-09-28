---
title: A3/k1 — cycle leak demo
kit_id: a3_shared_weak_cycles
version: 1.0
status: Draft
type: kata
---
## Goal
Demonstrate leaked pair when both sides own each other with `shared_ptr`.
## Task
Type `Node{ shared_ptr<Node> next; }`; create two nodes each owning the other; destroy scope; observe leak (ASan) / destructor not called.
## Acceptance
- [ ] Destructor logs do not fire; sanitizer reports leak.