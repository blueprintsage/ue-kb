---
id: niagara__respawn-character-polygon-spawn__v1
family: niagara
topic: respawn-character-polygon-spawn
version: 1
ue: ["5.3","5.4","5.5"]
status: draft
license: GPL-3.0-or-later
art_license: CC-BY
source:
- type: course
slug: sci-fi-vfx
part: part-1
tags: ["level:201","series:sci-fi-vfx","part:1","pack:sci-fi"]
assets: []
deps: ["materials__respawn-polygon-spawn-particles__v1"]
last_updated: 2025-09-21
---


# Respawn — Character Polygon Spawn (Niagara)


## Summary
Polygon burst around character silhouette.


## Steps
- Mesh distance field sample → burst ring emit.
- Sub-UV flipbook for shard sprites; orient to normal.


## QA
- Fixed timestep; LODs defined; scalability tiered.