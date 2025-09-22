# /niagara/performance__bounds-significance-gpu__v2.md
---
title: "Performance — Bounds, Significance & GPU (Unified)"
id: performance_bounds-significance-gpu_v2
type: lesson
tags: ["lesson","niagara","performance","bounds","lod","significance","gpu","unified","remix:original"]
---
## Overview
A practical pass to make FX cheap and predictable: fix bounds, apply significance/LOD rules that hold up in gameplay, and set sane GPU-sim budgets—without changing the look.
## Learning Goals
- Author stable **fixed bounds** and avoid surprise culling.
- Use **Significance** + **Scalability** to throttle cost instead of turning FX off.
- GPU sims: pool usage, clamp spawn, and keep memory predictable.
## Prerequisites
One working Niagara system; basic knowledge of scalability settings.
## Steps (outline)
1) **Bounds** — Simulate worst-case → capture in Preview → set **Fixed Bounds** (system & emitters) with +10–20% headroom; validate in Game view.  
2) **Significance** — Add Significance Handler (distance/visibility) → set renderer/emitters to reduce spawn on low significance; expose a **Quality** user param to bias.  
3) **LOD Rules** — Define 2–3 tiers (Near/Mid/Far): width/opacity curves lighten → heavy secondaries disabled in Far; verify readability snapshots.  
4) **GPU Sims** — Cap particles/sec; enable **Determinism** where possible; prefer **culled modules** over hard kills; use **fixed timestep** if jittery.  
5) **Pooling & Lifetime** — Add lifetime ceiling; soft-kill on stop; soak test 5 minutes, track peak particle counts.  
6) **Instrumentation** — Use Stat Niagara + overdraw view; log once per second peak counts; bake findings into MI/curve presets.
## Optimization: Ice Attack
- **DBuffer decals** cost: prefer short lifespan (<1.2 s) and small size; atlas where possible.
- **Translucency:** keep refraction OFF on Low; clamp blendable passes; cap total icicle meshes per burst.
- **GPU sims:** if using smoke/glints on GPU, target ≤ 5k max alive; fixed bounds to avoid cull pops.
## Optimization: Beams
- Fixed bounds span source↔target plus 20% margin; fork beams share bounds with primary.
- Significance: reduce fork rate first; clamp emissive at Far LOD; keep ground spark budget tiny.
## Add-on Pack — Big Plumes, Beams, Weather, Liquids, AOE
Plumes/Dust: one large fixed bounds or tiled volumes; prefer fewer larger sprites; cap GPU max alive (≤10k scene).  
Beams: bounds span src↔tgt +20%; reduce fork rate at Far LOD; clamp emissive.  
Weather: wind via MPC; Snow on CPU for collisions, GPU for storms; Far LOD disables secondaries.  
Liquids: strict pooling; kill after 2nd bounce; decals short-lived.  
AOE: budget by tier; disable ribbons/extra secondaries first; determinism ON when events drive gameplay.

## QA Checklist
No popping from bounds; significance never kills primary read; GPU peak stays under target; Far LOD is still readable at 30–40m; soak test shows no growth.
## Release Notes
v2 — merged significance/LOD notes, GPU gotchas, and bounds cookbook into a single workflow.
## Version notes
- Tested 5.1/5.3/5.4.  
- 5.1 GPU: enable **Fixed Bounds** early; slightly lower spawn to avoid culling spikes.  
- 5.3+: prefer **Significance Handler: DistanceAndVisibility**; tune per-renderer reduction rather than disabling systems.
