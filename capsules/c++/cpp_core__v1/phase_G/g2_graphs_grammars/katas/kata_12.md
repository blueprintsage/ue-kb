---
title: G2/k12 — Seeding & Reproducibility
kit_id: g2_graphs_grammars
version: 1.0
status: Draft
type: kata
---
## Objective
Centralize RNG seeding; ensure identical outputs when seed/params equal.
## Tasks
- Provide seed API; pass seed to all submodules; store seed in exports.
## Acceptance
- [ ] Bit‑stable outputs with fixed seed; decorrelated with new seeds.  
- [ ] Seed recorded in metadata for regression.