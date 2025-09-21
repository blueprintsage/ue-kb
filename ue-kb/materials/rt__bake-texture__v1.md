# Render Target — Bake to Texture
**Domain:** materials • **Level:** beginner • **Engine:** UE5

## Recipe
- After drawing to an RT, right-click the RT → **Create Static Texture**.
- Set compression (Masks/Grayscale/Default) and mipmaps as needed.
- Replace live RT in materials with the baked texture when you want fixed art.

## Checks
- Baked texture matches the RT look; no runtime dependency on the BP draw.
## Pitfalls
- Forgetting to set compression leads to washed colors or heavy files.
