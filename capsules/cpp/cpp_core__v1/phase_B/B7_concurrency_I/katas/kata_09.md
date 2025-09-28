---
title: B7/k9 — Git version stamping (semver-ish)
kit_id: b7_build_tooling
version: 1.0
status: Draft
type: kata
---
## Objective
Generate a config header from `git describe` and embed version/commit.
## Acceptance
- [ ] Binary prints version+commit; dirty tree marks `-dirty`; reproducible in CI.
