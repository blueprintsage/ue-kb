---
title: A13/k2 — trivial relocation
kit_id: a13_start_lifetime
version: 1.0
status: Draft
type: kata
---
## Goal
Relocate a buffer of Ts with memcpy only when proxy trait holds.
## Task
Define RelocT (trivial) and NonRelocT (non-trivial); test bulk move path selection.
## Acceptance
- [ ] memcpy used for RelocT only; NonRelocT uses move/construct.