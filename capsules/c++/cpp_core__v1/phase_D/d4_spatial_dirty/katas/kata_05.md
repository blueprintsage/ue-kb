---
title: D4/k5 — Broad-phase filter
kit_id: d4_spatial_dirty
version: 1.0
status: Draft
type: kata
---
## Goal
Use partition to cull candidate pairs before narrow collision.
## Task
Generate moving points; grid filter pairs; compare to naive pair count.
## Acceptance
- [ ] Candidate count << naive; results match within epsilon.