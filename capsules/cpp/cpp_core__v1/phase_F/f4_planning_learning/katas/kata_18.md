---
title: F4/k18 — Thompson Sampling (Beta/Gaussian)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Sample from posterior to balance explore/exploit via **Thompson sampling**.
## Task
Bernoulli rewards: Beta(α,β) per arm; draw θ_i~Beta and pick argmax. Gaussian rewards: Normal‑Gamma prior or Normal with known σ. Compare regret.
## Acceptance
- [ ] Thompson matches or beats UCB on noisy rewards.
- [ ] Posterior updates numerically stable; priors documented.