## Add-on Pack — Workflow, Control & Caching
Covers: pressure-relief vents, User Params + Sequencer, cache simulation, volume render tips, and render-res tricks.
**Intent/Outcome:** Direct fluids in gameplay/cinematics with deterministic control.

### Beats
- User Params & Sequencer → key `Sim_Enable`, `Flow_Intensity`, `Light_Channel`; record cache toggles.
- Cache Simulation → when to bake vs real-time; cache invalidation rules.
- Render Tips → path tracer notes; increase resolution only at render via MRQ overrides.

### Controls
- `Cache_Mode` (Off/Record/Playback), `Seed`, `Exposure_Clamp`.

### Performance/LOD
- Playback cheaper than live; keep cache sizes bounded; purge policy per level.

## Related
- Volumes & Lighting; Fundamentals (template).

## QA
- Cache playback equals live look within tolerance; Sequencer tracks named and scoped.

## Release Notes
- 2025-09-22: First pass (13–15, 41–42).
