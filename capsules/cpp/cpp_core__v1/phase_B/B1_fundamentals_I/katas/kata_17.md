---
title: B1/k17 — Enum Class & Bitflags
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Prefer `enum class`; implement safe bitflag helpers.
## Tasks
- Provide `operator|,&,^,~` for a flags enum; ensure no implicit to int.
## Acceptance
- [ ] Type‑safe flags compile; misuse requires explicit casts.