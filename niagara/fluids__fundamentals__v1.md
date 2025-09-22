## Add-on Pack — Fluids Fundamentals (Particles → Template)
Covers: Niagara particles intro (P1–P2), Content Examples tour, and a reusable Fluids Template.
**Intent/Outcome:** Understand particle lifecycles and spin up a clean fluids-ready system template.
**Prereqs:** UE5.3+, Niagara enabled; Project has Distance Fields on if you plan volume shading.

### Beats
- Particles 101 → update stacks, spawn/update order, and renderer sanity checks.
- Content Examples → locate baseline flame/smoke/water setups; note perf costs (overdraw, sim).
- Fluids Template → a starter NS with User Params: `FX_Scale`, `FX_Tint`, `Sim_Quality`, `Light_Channel`.

### Controls
- `Sim_Quality` (Low/Med/High) gates voxel size/iterations.
- `FX_Scale` drives bounds/emit rate; deterministic seed for capture.
- Renderer toggles: volumetric fog write, transmittance clamp.

### Performance/LOD
- Fixed bounds by scale tier; clamp max alive; prefer pooled components.
- Capture maps use fixed exposure and bloom clamp.

## Related
- Volumes & Lighting (setup), Workflow & Control (cache/seq).

## QA
- Template activates/destroys cleanly; bounds stable; Low tier renders acceptably.

## Release Notes
- 2025-09-22: First pass (Fluid Immersion 03–06).
