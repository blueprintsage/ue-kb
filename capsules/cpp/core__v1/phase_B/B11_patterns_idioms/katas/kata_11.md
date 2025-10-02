---
title: B11/k11 — Static initialization order fiasco (SIOF)
kit_id: b11_footguns
version: 1.0
status: Draft
type: kata
---
## Objective
Reproduce SIOF across TUs; fix with function-local statics or dependency injection.
## Acceptance
- [ ] Failure pre-fix on some platforms; post-fix deterministic init order verified in test.
