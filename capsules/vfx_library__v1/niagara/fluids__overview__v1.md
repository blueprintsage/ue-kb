## Add-on Pack — Niagara Fluids Overview (P1–P3)
Covers: Fluids intro Parts 1–3 (fundamentals, emitters, solvers, collision hooks).
**Intent/Outcome:** Know what toggles matter (voxel size, steps, dissipation) and their visual/readability impact.

### Beats
- Emitters & Sources → particles-as-sources vs mesh volumes; choosing resolution.
- Solvers → smoke/fire params (vorticity, buoyancy, dissipation) + stability guards.
- Collisions & Obstacles → DF/Raycast options; cheap vs accurate contacts.

### Controls
- `Voxel_Size`, `Time_Steps`, `Dissipation`, `Buoyancy`, `Vorticity`, `Temp_Factor`.
- Quality gates shift `Voxel_Size` and `Time_Steps` first.

### Performance/LOD
- Distance-based step reduction; shadowing off at Far; cap lighted volume count per scene.

## Related
- Full-Flow & Fire, Volumes & Lighting.

## QA
- Stability at max timestep; no NaNs; sim pause/resume consistent.

## Release Notes
- 2025-09-22: First pass (07–09).
