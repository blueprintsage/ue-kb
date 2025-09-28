---
title: A7 — Memory‑Mapped Files & Shared Memory
kit_id: a7_mmapped_sharedmem
version: 1.0
status: Draft
category: Resource Management
assets: []
dependencies: [a1_raii, a2_unique_ptr_deleters, a4_ownership_zoo]
---

## Objective
Use **memory‑mapped I/O** to view files or shared regions as arrays/spans with zero‑copy semantics; manage lifetimes and platform differences (POSIX `mmap`/`munmap` vs. Win `CreateFileMapping/MapViewOfFile`).

## Setup
- Tooling: Catch2; on Linux/macOS enable `-D_POSIX_C_SOURCE` as needed.
- Conditional compile: `#if _WIN32` path for Win32 APIs.

## Steps
1) **Map read‑only**: open file → map `PROT_READ` / `FILE_MAP_READ` → view as `std::span<std::byte const>`; verify size.
2) **Map read‑write**: ensure file is sized; map writable; modify region; flush (`msync` / `FlushViewOfFile`).
3) **Anonymous/shared**: create POSIX shared memory (`shm_open+ftruncate+mmap`) or Windows `PAGE_READWRITE` mapping; demonstrate two views seeing updates.
4) **Bounds safety**: wrap the mapping in a tiny RAII class exposing a `span<T>`; forbid re‑interpret casts that violate alignment.
5) **Resize hazards**: show that shrinking the backing file after mapping can SIGBUS/AV; prefer unmap+remap pattern.
6) **CoW maps**: map with `MAP_PRIVATE` (POSIX) to edit without writing back; verify on disk remains unchanged.
7) **Sync**: coordinate writer/reader with a named semaphore/mutex or file lock.

## Smoke Test
- [ ] Read/write mappings behave as expected; flush persists.
- [ ] No out‑of‑bounds access; unmap occurs exactly once.

## Blueprint Hook (TL;DR for BP users)
**What transfers:** treat large data blobs as **views** with explicit open/close and clear write‑back rules.  
**BP building blocks:** Streaming levels/tiles (load/unload), **Render Targets** for CPU↔GPU data, SaveGame for persistence.  
**Mini demo:** Open RT → draw N frames → save to texture → ensure release; Acceptance: no lingering RT memory after map change.

## Keep/Revert
KEEP: Resize hazard + CoW callouts.  
REVERT: Drop Windows path if target is POSIX‑only.