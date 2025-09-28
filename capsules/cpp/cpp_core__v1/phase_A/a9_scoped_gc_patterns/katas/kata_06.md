---
title: A9/k6 — GC root tree
kit_id: a9_scoped_gc_patterns
version: 1.0
status: Draft
type: kata
---
## Goal
Model a tree owned from one `unique_ptr` root; children hold observers only.
## Task
Build simple node tree; prove single-root destruction tears down entire graph.
## Acceptance
- [ ] All destructors fire in post-order; no cycles.