---
title: BR09/k1 — Hit once-only guard
kit_id: br09_projectiles
version: 1.0
status: Draft
type: kata
---
## Goal
Prevent duplicate hit processing.
## Given
Projectile with OnHit event.
## Task
Add `bHasHit` bool; on first hit set true, broadcast impact, disable collision, stop movement, start destroy timer. Ignore further hits.
## Acceptance
- [ ] Impact logs once per projectile.
- [ ] No physics spam or repeated damage.