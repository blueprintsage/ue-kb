---
title: F1/k20 — Deterministic Replay Logger
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Record minimal inputs (seed, decisions, external events) to replay a sim bit‑for‑bit.
## Task
Log per‑frame random seeds and external stimuli; on replay, drive agent loop from log and compare trajectories.
## Acceptance
- [ ] Trajectories exactly match baseline within float epsilon.
- [ ] Log size bounded; rotating buffer policy proven.