---
title: BR09/k3 — Lifetime & cleanup timing
kit_id: br09_projectiles
version: 1.0
status: Draft
type: kata
---
## Goal
Cleanly remove projectile after impact.
## Task
On first hit: disable collision, stop movement, spawn impact FX, destroy after 0.5s.
## Acceptance
- [ ] No lingering actors; subsequent hits from debris don’t trigger.