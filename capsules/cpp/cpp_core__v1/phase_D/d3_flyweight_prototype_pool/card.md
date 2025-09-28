---
title: D3 — Flyweight, Prototype, Object Pool
kit_id: d3_flyweight_prototype_pool
version: 1.0
status: Draft
category: Patterns
assets: []
dependencies: [d1_update_loop_component]
---


## Objective
Reduce memory + speed up creation by sharing **intrinsic state** (Flyweight), cloning **Prototypes**, and reusing objects via an **Object Pool**.


## Steps
1) Flyweight: share heavy data (mesh/material) across many light instances.
2) Prototype: clone preconfigured object graphs quickly.
3) Object Pool: pre‑allocate N; hand out/reclaim; guard double‑free.
4) Compare perf/memory vs naive new/delete per object.
5) Pool cleanup: bulk teardown in one step.


## Smoke Test
- [ ] Peak memory and creation time improve vs naive.


## Blueprint Hook
**What transfers:** keep shared data assets; pool actors/components; clone from templates.


## Keep/Revert
KEEP: pool guards; REVERT: skip prototype if not needed.