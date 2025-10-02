---
title: E4/k8 — Semi-Implicit Euler (Symplectic)
kit_id: e4_numerics_stability
version: 1.0
status: Draft
type: kata
---
## Objective
Use semi-implicit Euler to improve stability on oscillatory systems.
## Task
Update v ← v + dt*a(x), x ← x + dt*v; compare energy drift to explicit Euler on spring system.
## Acceptance
- [ ] Energy bounded for dt beyond explicit threshold (within reason).
- [ ] Phase error characterized; document tradeoffs.
## Keep/Revert
KEEP: velocity-updated-before-position. REVERT: position-first explicit step.