# PAT: Ribbon Basics
**Purpose:** Trails for sparks/energy strands.  
**Chain:** CPU emitter spawning points → **Ribbon Renderer** (Tangent from Velocity) → material with UV along length (V) and age (U).  
**Params:** Max Particles high enough; width over age curve.  
**Checks:** Continuous trail; width tapers; UVs map predictably.  
**Pitfalls:** Too few particles (gaps); wrong tangent/facing twists ribbons.
