---
title: G1/k8 — Histogram Match & Domain Remap
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---
## Objective
Match noise histogram to a target CDF and remap to usage domains (height/roughness/flow strength).
## Tasks
- Compute empirical CDF; map via inverse CDF of target; expose presets (sand, snow, rock).  
- Provide linear and curve‑based domain remaps.
## Acceptance
- [ ] CDF mapping verified within tolerance; no banding.  
- [ ] Remapped outputs in [0,1] (or chosen domain) with monotone mapping.