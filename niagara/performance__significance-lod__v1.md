# Performance — Significance & LOD
**Domain:** niagara • **Level:** advanced • **Engine:** UE5

## Goal
Keep FX cheap at distance or when off-screen.

## Recipe
- In **System Settings**: enable **Determinism** only if required. Configure **Fixed Bounds** to avoid culling pops.
- **Scalability**: set **Significance Handler** (Distance or Custom). Add **Emitter/Renderer LODs**: lower spawn, simpler materials, disable ribbons/mesh at far LODs.
- **Cull**: reduce update rate or pause when not rendered; use **Warmup** to avoid first-frame pops.

## Checks
- Far FX show fewer/cheaper particles; near FX stay full fidelity.

## Pitfalls
- Missing bounds → early cull; overusing determinism or heavy materials on GPU FX.
