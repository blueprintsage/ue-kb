---
title: F2/k8 — Utility Actions & Considerations
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Score actions using response curves (linear, logistic, power) and normalize.
## Task
Compute score = Π considerations; choose argmax; add floor to prevent starvation.
## Acceptance
- [ ] Chosen action matches hand-calculated maxima.
- [ ] Small input noise doesn’t cause thrash (hysteresis ≥ Δ).