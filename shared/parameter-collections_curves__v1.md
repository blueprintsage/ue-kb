# Parameter Collections & Curves (Global Control)
**Domain:** shared • **Level:** intermediate • **Engine:** UE5

## Goal
Drive many materials/FX at once and shape values smoothly.

## Recipe
- **Material Parameter Collection (MPC):** Create MPC with `Scalar GlobalIntensity`, `Vector Tint`. In materials, use **CollectionParameter** nodes. In BP: `Set Scalar Parameter Value (MPC)` to broadcast changes.
- **Niagara User Curves:** Add `Float Curve` in emitter/system (e.g., Size over Age). For shared shapes, use **Curve assets**; expose a **User Float** to scale curves at runtime.

## Checks
- One BP change affects multiple FX; curve edits immediately reshape timing.

## Pitfalls
- Name mismatches; MPC not referenced in a material; curve time not matching lifetime.
