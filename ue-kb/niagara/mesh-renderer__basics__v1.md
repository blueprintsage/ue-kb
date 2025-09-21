# Mesh Renderer — Basics
**Objective:** Render particles as meshes instead of sprites.
## Recipe
- Emitter: keep CPU for events; set **Renderer = Mesh**; pick a small mesh (sphere/low-poly shard).
- Align: **Facing Mode = Velocity**, (opt) **Z aligns with velocity**; size via **Mesh Scale** (random range).
- Material: use an unlit or lit material with vertex color support.
## Checks
- Particles render as meshes; scale/rotation vary; velocity facing reads clearly.
## Pitfalls
- Heavy meshes tank perf; use low-poly + instance-friendly materials.
