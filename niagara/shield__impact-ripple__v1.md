# Shield — Impact Ripple
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Recipe
- Static sphere mesh or SDF proxy; on hit, spawn ring ripple (sphere mask in material).
- Niagara: small burst of sparks on surface + short beam arcs to center.
- Material: sphere UV radial mask → ripple via time-based phase; add dithering.
## Checks
- Clean ring expanding on surface; brief sparks; fade-out with noise edge.
## Pitfalls
- Incorrect world-space mapping → ripple slides; fix by using WorldPosition.
