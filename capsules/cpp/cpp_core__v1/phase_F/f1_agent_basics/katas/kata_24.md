---
title: F1/k24 — PID Speed/Heading Controller
kit_id: f1_agent_basics
version: 1.0
status: Draft
type: kata
---
## Objective
Stabilize speed and heading using lightweight PID controllers feeding the steering combiner.
## Task
Target speed from higher‑level logic; compute throttle via PID(v_target−‖v‖). Heading PID uses shortest‑arc yaw error; convert to lateral accel.
## Acceptance
- [ ] Critically‑damped response (no overshoot) with tuned gains.
- [ ] Disturbance rejection within specified settling time.
## Keep/Revert
KEEP: clamp integral windup; derivative on measurement. REVERT: raw gains that overshoot wildly.