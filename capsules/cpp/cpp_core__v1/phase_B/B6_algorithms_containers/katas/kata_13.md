---
title: B6/k13 — Exception transparency in APIs
kit_id: b6_errors_contracts
version: 1.0
status: Draft
type: kata
---
## Objective
Define a public API rule: which functions may throw vs. must return error types.
## Acceptance
- [ ] Table marks each function as {throws|expected|error_code}; tests assert policy is followed via static wrappers.
