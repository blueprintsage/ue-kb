---
title: B3/k7 — ADL & Customization Points (swap)
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Implement free `swap` in your namespace and verify ADL finds it.
## Acceptance
- [ ] `using std::swap; swap(a,b)` picks custom overload.