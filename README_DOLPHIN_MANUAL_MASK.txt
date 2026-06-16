Dolphin update:
- Added assets/dolphin_spawn_mask.png generated from the user-marked red habitat areas.
- Dolphins spawn only inside the painted habitat mask.
- Spawn candidates must be visible in the camera/frustum before a pod is activated.
- Removed unsafe global relaxed spawning behavior.
- Dolphin jump arcs are tighter and vary slightly per dolphin within controlled thresholds.
- Existing land/lake/visual-water checks remain as backup safety guards.
