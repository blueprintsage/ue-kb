---
title: D1 — Update Method, Game Loop, Component
kit_id: d1_update_loop_component
version: 1.0
status: Draft
category: Patterns
assets: []
dependencies: []
---


## Objective
Practice the **Update Method** per object, a **fixed‑timestep game loop** (with accumulator & interpolation), and a minimal **Component** model (systems operating over components).


## Steps
1) Update method: entities expose `update(dt)`; system iterates and calls.
2) Fixed timestep: accumulator loop (dt_fixed), process multiple steps to catch up; interpolate render state.
3) Component model: entity holds component list; systems query by type and update in a stable order.
4) Determinism: validate same results across different frame times with fixed dt.
5) Pausing/time scale: support pause and global time scale.


## Smoke Test
- [ ] Varying real frame time yields identical physics steps vs serial baseline.
- [ ] Components attach/detach safely during iteration.


## Blueprint Hook (TL;DR for BP users)
**What transfers:** Tick in systems, not in every object; keep order deterministic; separate **simulate** vs **render**.
**BP building blocks:** `Tick` + **Subsystem** for central update; arrays of actors/components; time dilation.


## Keep/Revert
KEEP: accumulator + interpolation; REVERT: interpolation if not needed.