---
title: A13/k3 — type‑aware views
kit_id: a13_start_lifetime
version: 1.0
status: Draft
type: kata
---
## Goal
Switch between `span<std::byte>` and `span<T>` safely.
## Task
Check alignment/size, use `bit_cast` for PODs; otherwise stick to bytes.
## Acceptance
- [ ] No misaligned access; tests pass with odd offsets.