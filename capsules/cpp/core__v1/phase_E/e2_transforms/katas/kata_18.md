---
title: E2/k18 — World↔Screen Round‑Trip
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Verify world→clip→NDC→screen and back (via inverse VP) are consistent.
## Task
Project random points in front of camera; unproject back; compare.
## Acceptance
- [ ] Round‑trip error < 1e‑5 for in‑frustum points.
- [ ] Points behind near plane handled or rejected.
## Keep/Revert
KEEP: homogeneous divide; w>0 checks. REVERT: skip divide by w.