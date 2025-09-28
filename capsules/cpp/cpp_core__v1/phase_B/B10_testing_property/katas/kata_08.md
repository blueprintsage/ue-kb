---
title: B10/k8 — File descriptor RAII + retry on EINTR
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Wrap POSIX FD (or platform-appropriate handle) with RAII and safe read/write.
## Acceptance
- [ ] Close always happens; short read/write retried; errors surfaced as `error_code`.
