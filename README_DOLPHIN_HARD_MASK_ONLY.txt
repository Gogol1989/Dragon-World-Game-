Dolphin hard-mask-only update

Dolphin spawning now has one hard rule:
- dolphins can spawn only from precomputed samples inside assets/dolphin_spawn_mask.png
- samples are eroded inward before caching so pods stay safely inside the visible B-toggle boundaries
- spawning occurs only when the selected mask sample is visible in the camera
- no shoreline, landmask, lake, NASA-colour, zone-weighting, or relaxation fallback logic is used for spawning

Controls:
- Press B to toggle the exact dolphin territory overlay.

Jump arcs:
- Reduced travel distance and pod spread so dolphins remain inside the marked territories.
