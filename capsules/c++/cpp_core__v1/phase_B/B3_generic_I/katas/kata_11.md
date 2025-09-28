---
title: B3/k11 — Perfect Forwarding Helper
kit_id: b3_generic_I
version: 1.0
status: Draft
type: kata
---
## Objective
Write `make_with(Factory&& f, Args&&...)` using `std::forward`.
## Acceptance
- [ ] Preserves value categories; no extra copies in logs.