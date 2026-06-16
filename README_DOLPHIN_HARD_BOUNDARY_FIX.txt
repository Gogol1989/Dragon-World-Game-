Dolphin hard boundary fix
=========================

This build makes the hand-painted dolphin_spawn_mask.png the hard source of truth.

Key changes:
- Fixed CPU mask latitude sampling so image top = north and image bottom = south.
- Spawn cache is generated only from eroded pixels inside dolphin_spawn_mask.png.
- Dolphin pod members are checked at spawn start, splashdown, and along the full jump path.
- Runtime guard despawns any dolphin immediately if its current footprint leaves the mask.
- No legacy land/shore/lake/NASA-color fallback spawning path is used for dolphins.
- B still toggles the painted territory overlay.

Controls:
- B toggles dolphin spawn territory overlay.
