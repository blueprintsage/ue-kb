---
title: G2/k2 — Stochastic & Context‑Sensitive Rules
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Add weighted stochastic rules and simple context guards.
## Tasks
- Rules with weights (e.g., `A:0.7->AB`, `A:0.3->A`).  
- Context guard patterns like `<B>A` or `A>B` for left/right context.
## Acceptance
- [ ] Frequencies approximate weights over many runs.  
- [ ] Guards prevent illegal expansions; deterministic with seed.