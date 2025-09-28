---
title: E1/k14 — Project Onto Plane
kit_id: e1_vectors_spaces
version: 1.0
status: Draft
type: kata
---
## Objective
Project a point onto a plane (n·x = d) and compute signed distance.
## Task
Given p, plane (n,d) with unit n: p' = p − (n·p − d) n; distance = n·p − d.
## Acceptance
- [ ] p' lies on plane within 1e‑6.
- [ ] Distance sign flips when n reversed.
## Keep/Revert
KEEP: normalize n; stable dot. REVERT: unnormalized plane normal.