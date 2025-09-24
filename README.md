# Repo README — Capsules Workflow (v1.0)

**Scope:** All capsules (Blueprint, VFX, Non‑Niagara code)  •  **Date:** 2025‑09‑24 (CT)

---

## Overview

This repo uses **capsules** to ship work in small, testable batches. Each capsule has a **MANIFEST.md** for status tracking and an **EXPORT_QUEUE.md** listing files that are Ready to publish.

---

## Quick Start

1. Pick a capsule (e.g., `/capsules/blueprint_refresh__v1/`).
2. Open its `MANIFEST.md` and `EXPORT_QUEUE.md`.
3. Build/run items in UE. When an item passes **Acceptance**, set `status: Ready` and append its path to `EXPORT_QUEUE.md`.
4. Commit and push.

---

## Directory Layout

```
/capsules/
  blueprint_refresh__v1/      # BR01–BR18 (cards + katas)
  non_niagara_caps__v1/       # Phase A code packets (A0–A1…)
    phase_A/
      MANIFEST.md
      EXPORT_QUEUE.md
  niagara_playbooks__v1/      # VFX capture playbooks (cards only)
  vfx_library__v1/            # Unified VFX/BP/materials library
    MANIFEST.md
    EXPORT_QUEUE.md
    /niagara/ /materials/ /bp/ /meshes/ /patterns/ /shared/ /addons/ /delta/
```

---

## Capsule Workflow

* **Cards** = recipes (why/what/how) + Acceptance block.
* **Katas** (programming/BP only) = tiny proofs with their own Acceptance.
* **Statuses**: `Draft → Ready → Committed`.

**Ready checklist (per file):**

1. Acceptance passes in engine/tooling.
2. No TODOs/placeholders.
3. One‑line **Keep/Revert** note added.
4. `status: Ready` set in front‑matter.

**Export:** append the file’s path to `EXPORT_QUEUE.md`, then commit.

---

## Export Queue (source of truth)

* A path listed in `EXPORT_QUEUE.md` means the file is **Ready** to ship.
* CI or human scripts may read this list to prepare PRs/releases.
* Remove a path from the queue to pause shipping.

---

## Naming & Paths

* **Capsules**: `snake__version` (e.g., `vfx_library__v1`).
* **Files**: `domain/topic__detail__vN.md` (e.g., `niagara/flipbook__smoke-subuv-depthfade__v2.md`).
* **Katas**: `/katas/kata_01.md` per card; minimal acceptance tests.

---

## Lanes

* **Blueprint Refresh**: BR01–BR18 with 3 katas each; test in UE and mark Ready.
* **Non‑Niagara code (Phase A)**: A0–A1 packets now; more later.
* **Niagara Playbooks**: cards only; no katas; use capture Acceptance.

---

## Deprecated JSON

`kb_index.json` is deprecated. Use capsule **MANIFEST.md** and **EXPORT\_QUEUE.md** instead. If a tool requires JSON later, add a lightweight `capsules.index.json` that points to each capsule’s manifest/queue.

---

## Commit Message Hints

* Blueprint Batch: `feat(bp): add BR07–BR12 (cards) + k1 katas`
* VFX Library: `feat(vfx): add flipbook/ribbon/sequencer playbooks`
* Code Phase A: `feat(a1): raii + on‑ramp`
* Manifest‑only: `chore(manifest): update statuses and export queue`

---

## License & Credits

* Add your preferred LICENSE file.
* Credit external sources where appropriate (books, tutorials).
* Internal mantra: *“This is me, and I keep marching.”*
