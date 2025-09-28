---
title: B10/k9 — mmap RAII wrapper (portable sketch)
kit_id: b10_resources
version: 1.0
status: Draft
type: kata
---
## Objective
Map a file region with RAII; ensure unmap on destruction; document portability.
## Acceptance
- [ ] Access works; unmap always called; alignment/size rules asserted; Windows note if applicable.
