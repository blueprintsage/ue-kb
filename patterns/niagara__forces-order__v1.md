# PAT: Forces Order (Stable Motion)
**Purpose:** Apply forces/noise before velocity solve for smooth motion.  
**Update stack order:** Add forces (e.g., Curl Noise 5–20) → Drag 0.2–0.5 → SolveForcesAndVelocity → Integrate → (Color/Size over Life).  
**Checks:** Changing Drag predictably dampens drift; no jitter.  
**Pitfalls:** Drag before forces weakens effect; duplicated solvers double-integrate.
