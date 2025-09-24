---
title: BR02 — Input & Timelines
kit_id: br02_input_timelines
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR02_Input_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Create a sprint mechanic using a Timeline for smooth acceleration/deceleration, with input mappings.


## Setup
- Project inputs: `Sprint` (Action), `SprintAxis` (Axis optional)
- Player BP variable: `SpeedAlpha` (0..1)


## Steps
1) Add `Timeline_Sprint` (float track 0→1 in 0.25s; reverse on release).
2) On `InputAction Sprint (Pressed)`: Play `Timeline_Sprint`; on Released: Reverse.
3) On tick from Timeline: Lerp `WalkSpeed` between 300 and 600 using `SpeedAlpha`.
4) Optional: camera FOV Timeline for subtle zoom.


## Acceptance
- [ ] Speed blends smoothly on press/release.
- [ ] No speed drift after multiple toggles.


## Keep/Revert
KEEP: Timeline-driven blend.
REVERT: Swap to Curves for tweakable profile.