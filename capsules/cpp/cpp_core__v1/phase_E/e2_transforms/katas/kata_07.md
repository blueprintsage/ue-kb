---
title: E2/k7 — Screen→World Ray
kit_id: e2_transforms
version: 1.0
status: Draft
type: kata
---
## Objective
Generate a world‑space ray from screen pixel (x,y) using inverse view‑projection.
## Task
Map (x,y)→NDC; unproject near & far; ray = normalize(Pfar−Pnear).
## Acceptance
- [ ] Ray hits a test plane at expected world Z.
- [ ] Works across aspect changes and FOVs.
## Keep/Revert
KEEP: use homogeneous divide after inverse. REVERT: skip w‑divide.