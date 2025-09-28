---
title: B6/k21 — errno boundary (C interop) without leaks of globals
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Wrap a C API that uses `errno`, converting to `error_code` safely.
## Acceptance
- [ ] `errno` captured immediately and translated; no global state leaks; tests simulate two distinct errno values.
