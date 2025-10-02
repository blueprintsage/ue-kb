---
title: F2/k22 — Diminishing Returns & Cooldowns (Utility)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Discourage over‑repeating the same action by applying **diminishing returns** and action cooldowns to utility scores.
## Task
Track recent action usage u∈[0,1]; score' = score * (1−γ u); u decays by EMA; enforce cooldown windows per action.
## Acceptance
- [ ] Action diversity index increases vs baseline.
- [ ] Cooldown prevents immediate re‑entry; hysteresis avoids thrash.
## Keep/Revert
KEEP: EMA decay with half‑life; per‑action cooldown map. REVERT: hard bans only (stalls planner).