---
id: bp__vfx-lib__effect-spawn-router__v1
family: bp
topic: vfx-lib__effect-spawn-router
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["datatable","router","spawn","series:sci-fi-vfx","part:3"]
assets: []
deps: []
last_updated: 2025-09-21
---


# BP VFX Library — Effect Spawn Router


## Summary
Centralized spawn API: data‑driven Niagara spawns with user‑param injection and debug.


## DataTable Schema
`EffectID`, `System`, `UserParams(JSON)`, `ScalabilityTag`, `DefaultBoundsScale`.


## API
`RouteEffect(EffectID, Context)` → handle
- `Context`: Transform, TeamColor, Seed, WarmupPreset, BoundsScale.
- If `Seed` present → push to system param and enable fixed tick for duration.


## Debug
`VFXRouter.Log` bool toggles spawn prints with resolved params.