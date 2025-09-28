---
title: A4/k2 — enforce non‑null with gsl::not_null
kit_id: a4_ownership_zoo
version: 1.0
status: Draft
type: kata
---
## Goal
Prevent null observers at the boundary.
## Task
Add an API taking `gsl::not_null<Widget*>`; verify passing nullptr fails to compile or asserts in tests.
## Acceptance
- [ ] Boundary rejects null; happy path works.