---
title: F2/k21 — Resource Claiming & Leases (Multi‑Agent)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Prevent multiple agents from choosing the same target by adding **claims** with time‑limited leases.
## Task
Implement claim(key, agent, ttl) on the blackboard; auto‑expire via TTL; decisions check claim before selecting a target; support renew/release.
## Acceptance
- [ ] Zero double‑claims in randomized stress (≥100 agents, ≤50 resources).
- [ ] Expired leases free targets without manual cleanup.
## Keep/Revert
KEEP: monotonic clock + TTL; atomic compare‑and‑swap claim. REVERT: claim via naive set/get race.