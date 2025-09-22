## Add-on Pack — Volumes, Lighting & Atmospherics
Covers: Volume lighting/blank level setup, ground fog + particles-as-sources, light scattering/channels/clouds.
**Intent/Outcome:** Stand up readable fog/cloud volumes with predictable lighting.

### Beats
- Blank Level → exposure fixed, fog enabled, shadow maps budgeted.
- Ground Fog → particle emitters as sources (density/temperature masks).
- Light Scattering → per-light channels to isolate FX lights; cloud layering.

### Controls
- `Light_Channel` (int), `Volume_Shadow_Quality`, `Fog_Density`, `Fog_Anisotropy`.
- Optional: exposure clamp track in Sequencer.

### Performance/LOD
- Far LOD removes secondaries; reduce shadowed volume list dynamically.

## Related
- Fundamentals (template), Workflow & Control (Sequencer).

## QA
- No over-bright/bloom blowouts; fog reads in grayscale at Far.

## Release Notes
- 2025-09-22: First pass (10–12 + 11 ground-fog).
