---
title: G2/k6 — Cellular Automata Caves
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Generate caves with birth/survival rules, then smooth and connect components.
## Tasks
- Start from random fill; iterate CA; remove small components; optionally widen corridors.  
- Ensure single connected component.
## Acceptance
- [ ] One giant component after connect; tunable roughness.  
- [ ] No 1‑tile spikes after cleanup.