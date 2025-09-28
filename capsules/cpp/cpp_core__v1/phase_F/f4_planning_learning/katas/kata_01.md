---
title: F4/k1 — World State Encoding (Bitset/Mask)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Encode boolean world facts as bitmasks for fast precondition/effect checks.
## Task
Define `State { uint64 on, off; }` or bitset; precondition holds if `(s & on)==on && (~s & off)==off`. Apply effects via set/clear masks.
## Acceptance
- [ ] Precondition/effect checks branch‑light and pass unit tests.
- [ ] Supports ≥64 facts with extension mechanism.