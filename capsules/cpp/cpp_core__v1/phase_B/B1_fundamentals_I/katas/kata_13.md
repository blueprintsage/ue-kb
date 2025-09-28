---
title: B1/k13 — Small Buffer Optimization (SBO) Intro
kit_id: b1_fundamentals_I
version: 1.0
status: Draft
type: kata
---
## Objective
Implement a minimal SBO string/vector to see ownership transitions.
## Tasks
- Inline small data; heap on growth; track which storage is active.
## Acceptance
- [ ] Moves never allocate when size ≤ SBO; copies behave correctly.