---
title: B1/k9 — noexcept Moves & Strong Exception Safety
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Mark moves `noexcept` when valid to enable vector reallocation optimizations.
## Tasks
- Provide move ops `noexcept`; write test that vector growth prefers move over copy.
## Acceptance
- [ ] No throw from moves; capacity growth uses moves.