## Add-on Pack — Meteor (Fluid Plume)
Covers: meteor setup (source forces, hot plume, debris handoff) and capture beats.
**Intent/Outcome:** A readable meteor trail/impact stack using fluids + classic FX.

### Beats
- Source → high-velocity inject; temperature spike; plume rise with buoyancy.
- Debris → switch to ribbons/meshes post-impact; scorch decal optional.
- Capture → fixed exposure; 1–2 frame emissive spike on impact.

### Controls
- `Inject_Temp`, `Buoyancy`, `Dissipation`, `Debris_Rate`.

### Performance/LOD
- Plume voxel size scales by distance; debris on CPU for collisions, GPU for storm fields.

## Related
- Full-Flow & Fire; Hit/Impact — Sparks & Debris.

## QA
- Trail continuity at camera cuts; bounds stable along arc.

## Release Notes
- 2025-09-22: First pass (22 Meteor).
