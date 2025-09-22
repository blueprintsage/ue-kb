---
id: shared__parameter-collections_curves__v1
family: shared
topic: parameter-collections_curves
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["mpc","curves","tuning","series:sci-fi-vfx","part:3"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Parameter Collections & Curves (Global Control)


## Summary
Global timing/color control for coordinated effects.


## MPC Keys
`VFX_TeamColor`, `VFX_GlobalGlow`, `VFX_TimeScale`.


## Curves
Centralize spawn/fade/rim curves to update multiple effects in one place.


## BP Bridge
On router spawn, push MPC values; local user params override MPC when set.