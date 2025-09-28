---
title: G1/k1 — Perlin Noise 2D/3D (Permutation Table)
kit_id: g1_noise_fields
version: 1.0
status: Draft
type: kata
---

## Objective
Implement classic **Perlin noise** with fade, hash, gradient sets — 2D and 3D — with optional **tiling period P** and **seeded** permutation.

## Tasks
1. **Permutation table:** Build `perm[512]` by shuffling 0..255 with a seed (Fisher–Yates), then duplicate (`perm[i+256]=perm[i]`).
2. **Gradients:**
   - 2D: use 8 unit gradients (e.g., (±1,0),(0,±1),(±1,±1)/√2) via hash→index.
   - 3D: use Ken Perlin’s 12 vectors (edges of cube) via hash→index.
3. **Fade & lerp:** `fade(t)=6t^5−15t^4+10t^3`; trilinear/ bilinear interpolation of dot products.
4. **Tiling (optional):** For period `P>0`, wrap lattice indices `i%P` and access gradients via `(i%P)&255` so samples tile every `P` units.
5. **APIs:** Implement `perlin2(x,y, seed, period=0)` and `perlin3(x,y,z, seed, period=0)` returning roughly `[-1,1]`.
6. **Determinism:** Same `(x,y,seed,period)` yields identical value; different seeds change the field.

## Acceptance
- [ ] **Tiling:** For `period=P>0`, values match at (0,0) and (P,0), (0,P), (P,P) (and 3D analog).
- [ ] **Range/mean:** Over a large grid (256×256), mean ∈ [−0.05, 0.05]; values bounded in `[-1.2, 1.2]` before normalization.
- [ ] **Smoothness:** First derivatives continuous (no blocky artifacts); no visible seams at tile boundaries.
- [ ] **Deterministic:** Fixed seed reproduces identical image; changing seed changes structure.

## Notes
- Use integer lattice: `xi=floor(x)`, `xf=fract(x)` etc.; hash corners via `perm[perm[xi]+yi]` pattern.
- Normalize gradients if you include diagonals; or scale contributions so variance is reasonable.
- For performance, prefer integer masking `& 255` over `% 256`.

## Minimal Test (pseudocode)
```cpp
auto img = Image(256,256);
for y in 0..255:
  for x in 0..255:
    v = perlin2(x*freq, y*freq, seed=1337, period=64);
    img(x,y) = 0.5f * (v + 1.0f);
// Assert tiling:
assert(perlin2(0,0,1337,64) == perlin2(64,0,1337,64));
assert(perlin2(0,64,1337,64) == perlin2(64,64,1337,64));