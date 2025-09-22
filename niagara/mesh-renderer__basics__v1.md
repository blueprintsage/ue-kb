# Mesh Renderer — Basics
**Objective:** Render particles as meshes instead of sprites.
## Recipe
- Emitter: keep CPU for events; set **Renderer = Mesh**; pick a small mesh (sphere/low-poly shard).
- Align: **Facing Mode = Velocity**, (opt) **Z aligns with velocity**; size via **Mesh Scale** (random range).
- Material: use an unlit or lit material with vertex color support.
## Preset: Icicle Mesh Particles
- **Spawn:** surface or point burst; Rate 0, Burst 6–12 on impact; random yaw; pitch aligns to normal.
- **Scale:** non-uniform (Z 1.4–2.0); size over life → slight shrink.
- **Material:** M_IceCore; optional shell pass disabled beyond 20 m (significance).
- **Collision:** simple scene depth; damped bounce 0.1–0.2; kill on 2nd hit or after 1.0 s.
- **Perf:** fixed bounds; cap particles/sec; pool bursts.

## Checks
- Particles render as meshes; scale/rotation vary; velocity facing reads clearly.
## Pitfalls
- Heavy meshes tank perf; use low-poly + instance-friendly materials.
