---
title: B5/k26 — split view (tokenize) and join_back
kit_id: b5_ranges
version: 1.0
status: Draft
type: kata
---
## Objective
Tokenize a string using `views::split` (including empty fields) and then rejoin with a delimiter using `views::join_with` (or materialize + join helper), handling lifetimes safely.
## Acceptance
- [ ] Splitting "a,,b,c" by ',' yields ["a", "", "b", "c"] (empty preserved).
- [ ] Rejoining tokens reproduces the original (or expected normalized) string.
- [ ] No dangling views: tests pass when source storage outlives the pipeline.
