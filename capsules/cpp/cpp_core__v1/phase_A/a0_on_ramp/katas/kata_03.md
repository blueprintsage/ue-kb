kata_03.md---
title: A0/k3 — same‑bytes (bit_cast)
kit_id: a0_on_ramp
version: 1.0
status: Draft
type: kata
---
## Goal
Use `std::bit_cast` to inspect representation safely.
## Task
Round‑trip a POD to bytes and back; verify equality.
## Acceptance
- [ ] Static asserts compile; runtime checks pass.