# Sub-UV Fire/Smoke — BlackBody Emissive
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Goal
Layered flame (Sub-UV) with smoke, tone-map-safe emissive using BlackBody.
## Setup
- **Emitter A (Flame):** Sprite, Sub-UV 8×8, Spawn Burst + low SpawnRate, Init Size random (cone), Velocity stretch, ColorOverLife warm→hot.
- **Emitter B (Smoke):** Sprite, soft flipbook or noise UV-pan, larger size, lower alpha, longer lifetime, Drag + Curl.
- **Material (Flame):** BlackBody(tempK) * intensity; tempK from Particle.Color.R (0–1 → 1000–4000K remap). Add depthfade; clamp emissive to stay filmic.
## Tips
- Drive `tempK` by **Age** or a curve; use **SubImage Blend** for smooth Sub-UV; ensure smoke sorts behind flame; cap total overdraw in views.
