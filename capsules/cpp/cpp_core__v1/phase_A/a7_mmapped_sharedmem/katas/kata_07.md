---
title: A7/k7 — named sync
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
type: kata
---
## Goal
Coordinate writer/reader updates.
## Task
Use named semaphore (POSIX) or named mutex/event (Win) around writes.
## Acceptance
- [ ] No torn reads; readers see coherent states.