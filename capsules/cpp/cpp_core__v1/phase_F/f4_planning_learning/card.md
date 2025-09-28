---
title: F4 — Planning & Learning (GOAP, MCTS/UCT, Bandits)
kit_id: f4_planning_learning
version: 1.0
status: Draft
category: AI
assets: []
dependencies: [f1_agent_basics, f2_decisions, f3_pathfinding]
---

## Objective
Plan, decide, and adapt: **GOAP** for symbolic planning, **MCTS/UCT** for look‑ahead in uncertain domains, and **multi‑armed bandits** for data‑driven action selection.

## Steps
1) **GOAP core:** world state (bitset), actions (preconditions/effects/costs), A* on state space.
2) **Execution:** plan monitor, replanner on failure, partial‑order effects, resources/cooldowns.
3) **MCTS:** selection (UCT), expansion, simulation (rollouts), backprop; transposition table.
4) **Bandits:** ε‑greedy, softmax/boltzmann, UCB1; non‑stationary via EMA.
5) **Parity & budget:** compare methods on scenarios; enforce tick budget & determinism.

## Smoke Test
- [ ] GOAP hits goals with minimal cost on solvable domains; replans on blocked actions.
- [ ] MCTS improves policy with more iterations; bandits converge to high‑reward arms.

## Blueprint Hook (TL;DR)
**Transfers:** UE5 BT Task node calls a GOAP planner (C++ or BP) to fill a blackboard with an action queue; optional **MCTS selector** for combat moves; **Utility/Bandit** node to pick abilities. **Mini demo:** Door‑key‑treasure domain with blocking; planner replans if door gets re‑locked.