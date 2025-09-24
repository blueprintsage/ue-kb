# Custom Module — Reusable Asset (201)
**Domain:** niagara • **Level:** intermediate→advanced • **Engine:** UE5

## Goal
Promote scratchpad logic to a reusable **Module Script asset**.

## Recipe
- Open your Scratchpad → **Promote to Asset** → name `NM_ScaleVelocity`.
- In the script: define **Inputs** (`Scale`, `ClampMin/Max`) with tooltips & categories.
- Add **Usage Hints** (Spawn/Update). Compile. Place in multiple emitters/systems.

## Checks
- Dropping `NM_ScaleVelocity` into another system works identically; inputs appear neatly grouped.

## Pitfalls
- Missing usage flags; not versioning inputs → downstream graphs break.
