# Ribbon Renderer — Setup
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Recipe
- CPU emitter spawning points from a moving source (or Spawn Per Unit).
- **Ribbon Renderer**: Tangent from Velocity; set **Link Order** (Source or Age); width over age curve.
- Material: UV along length (V) and over age (U); optional color from Particle Color.

## Checks
- Continuous trail with tapered width; no twisting.
## Pitfalls
- Too few particles → gaps; wrong tangent/facing → corkscrew twists.
