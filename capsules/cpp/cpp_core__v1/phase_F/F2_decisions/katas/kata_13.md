---
title: F2/k13 — Latent Actions & Interruption Contracts (BT)
kit_id: f2_decisions
version: 1.0
status: Draft
type: kata
---
## Objective
Implement **latency‑bearing actions** (e.g., play montage, wait, move) that return Running; support clean cancel/resume.
## Task
Action stores local state (start time/handles). On abort, run OnCancel to free resources; on resume, continue or restart per policy.
## Acceptance
- [ ] No resource leaks on abort; correct status transitions.
- [ ] Resume policies behave as configured (resume/restart/skip).