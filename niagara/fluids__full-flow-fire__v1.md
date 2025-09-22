## Add-on Pack — Full-Flow & Fire Recipes
Covers: small/full flow, wisps/ink-in-water, big fire + custom gradient, cars-on-fire, embers; plus scenario riffs (missile raindrop, rocket launch, rotor cleaning, shock wave, aircraft/tree fires, drifting car, “Oppenher”, Arctic Flare).
**Intent/Outcome:** Practical presets with safe ranges and capture-ready polish.

### Beats
- Full Flow Techniques → stable step/voxel combos; boundary conditions; caching when needed.
- Fire Presets → temperature→color gradient authoring; emissive clamps; ember spawn hooks.
- Scenario Patterns → input forces and emit shapes (cones, streaks, volumetric shells).

### Controls
- `Flow_Intensity`, `Gradient_LUT`, `Emissive_Clamp`, `Ember_Rate`, `Shock_Radius`.

### Performance/LOD
- Short-lifetime secondaries; ribbon/mesh debris off at Low; cache heavy sims.

## Related
- Meteor FX (impact plume), Volumes & Lighting.

## QA
- No banding in gradients; ember pool limits respected; step changes don’t flicker.

## Release Notes
- 2025-09-22: First pass (16–22, 23–33, 39–42, 32–33 Arctic Flare noted duplicate).
