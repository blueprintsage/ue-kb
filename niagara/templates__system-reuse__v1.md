# Templates & Reuse — System Patterns
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Goal
Ship faster by cloning proven setups.

## Recipe
- Create `/VFX/Templates/` systems: `NS_FlipbookSmoke`, `NS_RibbonSpark`, `NS_ImpactHit`, each with sane **User.*** parameters and LODs.
- Document required materials/flipbooks; keep consistent param names across templates.
- When starting new FX, **Duplicate** a template and tailor only what’s unique.

## Checks
- New effects stand up in minutes; BP hooks work without renaming.

## Pitfalls
- Divergent param names across templates; missing dependencies (materials/curves).
