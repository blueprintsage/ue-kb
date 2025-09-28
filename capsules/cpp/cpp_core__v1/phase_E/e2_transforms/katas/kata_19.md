---
title: E2/k19 — Handedness Conversion (RH↔LH)
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Convert transforms between right‑handed and left‑handed conventions.
## Task
Show that flipping the Z axis changes handedness; adjust projection and view accordingly.
## Acceptance
- [ ] Forward vectors, culling, and depth tests remain correct.
- [ ] No mirroring of geometry after conversion.
## Keep/Revert
KEEP: flip consistent axes in both view and projection. REVERT: flip only one space.