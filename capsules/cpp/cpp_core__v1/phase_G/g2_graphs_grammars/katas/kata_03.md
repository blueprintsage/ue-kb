---
title: G2/k3 — Wave Function Collapse (Tiled, Simple)
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Implement basic WFC with tiles, adjacency rules, entropy priority queue, and propagation.
## Tasks
- Represent superposition per cell; pick lowest‑entropy cell; collapse per weighted tile; propagate constraints.  
- Stop on solution or contradiction.
## Acceptance
- [ ] No rule violations; entropy never negative.  
- [ ] Converges on valid tile sets; fails fast on invalid ones.