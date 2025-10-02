---
title: F2/k9 — Utility Arbitration & Hysteresis
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Prevent rapid toggling by adding entry/exit thresholds and cooldowns to utility selection.
## Task
Maintain last action and add Δ_on/Δ_off; update only if score improves by margin.
## Acceptance
- [ ] Action switches drop ≥50% in noisy stimuli.
- [ ] Latency bounds documented and within spec.