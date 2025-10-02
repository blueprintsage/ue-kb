---
title: A4/k3 — one owner, many observers
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Maintain one `unique_ptr<Widget>` and expose observers safely.
## Task
Container keeps `unique_ptr<Widget>`; callers get `Widget&`/`Widget*`; confirm no copies of owners escape.
## Acceptance
- [ ] Static analysis/tests verify ownership doesn’t leak.