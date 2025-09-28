---
title: BR13 — Advanced Nodes & Editor Hygiene
kit_id: br13_adv_nodes
version: 1.0
status: Draft
category: Blueprint
deliverables:
demo_map: BR13_AdvNodes_Map
media:
- type: screenshot
views: [BEAUTY]
assets: []
dependencies: []
---


## Objective
Use advanced nodes (Select, Map/Set ops, ForEach, Sequence/DoOnce, Gate) and apply editor hygiene (comments, reroute, collapse to function).


## Steps
1) Build a small decision graph with **Select** and **Maps/Sets** for lookup.
2) Replace Tick chains with **DoOnce/Sequence/Gate** where appropriate.
3) Collapse a repeated section into a **Pure Function**; add reroute/regions and comments.


## Acceptance
- [ ] No Tick polling where events suffice.
- [ ] Repeated logic refactored to function; graph is readable.


## Keep/Revert
KEEP: Function collapse pattern.
REVERT: Add Macro example later if needed.