---
title: F4/k23 — MCTS with Policy Priors & Value Fn (AlphaZero‑Lite)
kit_id: f4_planning_learning
version: 1.0
status: Draft
type: kata
---
## Objective
Bias MCTS using a **policy prior** over actions and a **value function** to cut rollout depth.
## Task
Use PUCT: select with `Q + c_puct * P * sqrt(N)/(1+n)`; bootstrap leaf value from V(s) instead of/random rollout; compare to vanilla UCT.
## Acceptance
- [ ] Same/better decision quality at lower iteration budgets.
- [ ] No policy collapse: exploration term keeps diversity (tuned c_puct).
## Keep/Revert
KEEP: normalize priors; clip V to bounds. REVERT: trust raw, unnormalized priors.