# Material Instances — Fast Tuning Workflow
**Domain:** materials • **Level:** beginner • **Engine:** UE5
## Setup
- Master has only parameters; expose scalars/vectors/texture slots with categories.
## Workflow
- Create **MI_*** per effect; tune in PIE with **Property Matrix**; bind key params to MPC for global sweeps.
- Lock values: rename tested params with suffix `_LOCK` (doc-only) and copy to curve/MPC if they drive many FX.
## Tips
- One master per “look” family (smoke, beam, decal); instances per use-case.
