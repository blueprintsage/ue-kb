# Templates & Reuse — System Patterns
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5

## Goal
Ship faster by cloning proven setups.

## Recipe
- Create `/VFX/Templates/` systems: `NS_FlipbookSmoke`, `NS_RibbonSpark`, `NS_ImpactHit`, each with sane **User.*** parameters and LODs.
- Document required materials/flipbooks; keep consistent param names across templates.
- When starting new FX, **Duplicate** a template and tailor only what’s unique.

## Add-on: References & Sketching (Pre-production)
- Block quick thumbnails for muzzle/trail/impact; list primary read per beat; note color/contrast guardrails.
- Keep a tiny ref board per biome (indoor, desert, snow) to pre-decide emissive caps and decal lifetimes.
## Add-on Pack — References & Sketching (Pre-production)
### Sketch first
Thumb muzzle / trail / impact; declare **primary read per beat**; set color/contrast guardrails (biome-aware). Keep a tiny ref board per biome (indoor, desert, snow) to pre-decide emissive caps & decal lifetimes.


### System template
`NS_TPL_Projectile` with emitters: `Muzzle`, `Trail_Ribbon`, `Impact_Burst`, `Impact_Smoke`. User Params: `FX_Scale`, `FX_Tint`, `FX_Intensity`. Event names: `FX.Projectile.Muzzle/Trail/Impact` (router-friendly). Bounds preset curve by `FX_Scale`.


### Reuse pattern
Duplicate → rename with prefix (`NS_Proj_<style>`), swap materials via **MIs**, keep module list identical, only tune curves/params. Log deltas in a 3-line note at file top (`ChangeLog:`).


### DT + Router
DataTable drives: System asset, `FX_Scale`, `FX_Tint`, quality gates. BP router reads row by tag (e.g., `FX.Projectile.Impact`) and applies user params before `Activate`.

## Add-on Pack — Reference Boards & Style Targets
Build 3 mini boards (indoor, desert, snow). For each: mark **primary read** and emissive caps.
Add heatmaps (where the eye should look) and do a quick grayscale pass to validate silhouette.
Lock a 3–5 color palette per biome; save as LUT or Material Param Collection swatches.
Name presets `stylized/<biome>/<effect>` so router + DT can swap cleanly.
### Folders & naming
`/VFX/Projectiles/<style>/NS_*`, materials under `/VFX/Materials/MI_*`, DTs in `/VFX/DT/DT_VFX_Projectiles`. Keep short, lowercase, dash-separated names for textures/flipbooks.
## Checks
- New effects stand up in minutes; BP hooks work without renaming.

## Pitfalls
- Divergent param names across templates; missing dependencies (materials/curves).
