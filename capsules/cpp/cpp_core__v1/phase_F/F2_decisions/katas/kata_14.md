---
title: F2/k14 — Subtree Instancing & Parameter Binding
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Reuse behavior by instancing a **subtree** with bound parameters (e.g., target key, timeout, radius).
## Task
Define a generic "MoveToAndInteract" subtree; bind keys/values per caller; verify isolation between instances.
## Acceptance
- [ ] Instances do not leak state across callers.
- [ ] Parameter overrides visible only inside subtree.