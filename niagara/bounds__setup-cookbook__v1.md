# Niagara Bounds — Setup Cookbook
**Domain:** niagara • **Level:** intermediate • **Engine:** UE5
## Why
Wrong bounds = pop-in/cull. Fix once per system.
## Steps
- In Preview, crank spawn/velocity to worst-case; in **Bounds** set **Use Fixed** and pad (10–25%).
- For moving FX (ribbons/trails), expand along motion axis; for portals, use ring radius * 1.3.
- Validate in **Stat Niagra** and fly camera around; no culling when off-center.
