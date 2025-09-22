---
id: niagara__determinism__warmup-seeds__v1
family: niagara
topic: determinism__warmup-seeds
version: 1
ue: ["5.3","5.4","5.5"]
status: stable
license: GPL-3.0-or-later
art_license: CC-BY
tags: ["determinism","warmup","bounds","series:sci-fi-vfx","part:3","source:book:butler"]
assets: []
deps: []
last_updated: 2025-09-21
---


# Determinism & Warmup — Seeds That Behave


## Summary
Predictable starts and repeatable beats using explicit seeds and warmup presets.


## Seed Discipline
- Per‑system `User.Seed`; per‑emitter offset: `Seed + EmitterIndex * 131`.
- Expose `Seed` on BP router context for sync shots.


## Warmup Presets
- None=0 · Short=8 · Medium=16 · Long=32 frames. Choose per effect; document in card.


## Tick Modes
- **Cinematic:** fixed tick + preset warmup.
- **Gameplay:** variable tick normally, switch to fixed for hero moments.


## QA
Capture cold‑start frames to catch flipbook one‑frame jumps; correct with warmup.