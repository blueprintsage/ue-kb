# Meteor — Trail + Impact
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- **Trail**: CPU points spawning while actor moves (Spawn Per Unit), **Ribbon Renderer** with smoky material (DepthFade + UV pan).
- **Core sparks**: GPU sprite or CPU ribbon for hot center streaks.
- **Impact event**: on collision → **Event Handler** spawns **Hit Impact** system (reuse previous card) at location/normal.
- Parameters: User floats for **Trail Density**, **Heat Distortion Strength**, **Impact Intensity**.

## Checks
- Smooth continuous trail with tapered width; impact triggers once with sparks/debris burst.

## Pitfalls
- Missing event bind = no impact; ensure collision is CPU for event emission.
