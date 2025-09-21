# Impact Decals — Spawn on Hit
**Domain:** materials • **Level:** intermediate • **Engine:** UE5

## Goal
Stamp scorch/mark decals at impact locations.

## Recipe
- Make **Deferred Decal** material (Domain: Deferred Decal). Pack albedo/roughness/normal as needed.
- In BP (OnHit/LineTrace): **Spawn Decal at Location** (material, size, life span) using hit `Location` and `Impact Normal` (build a rot from normal).
- Optional: pair with **Hit Impact** Niagara system for sparks/debris.

## Checks
- Decal aligns with surface; fades over lifespan if set.

## Pitfalls
- Wrong **Decal Blend Mode** → no visible effect; tiny size on large surfaces.
