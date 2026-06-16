Dolphin offshore spawning fix
- Dolphins now require a strict multi-ring open-ocean clearance test around the spawn and jump path.
- Increased minimum shore distance and removed relaxed fallback spawning.
- Added a visual ocean classifier that samples the NASA atlas/base texture, so dolphins cannot spawn on brown/green/white land even if the legacy land mask is slightly misregistered.
- Runtime safety still hides any active dolphin that crosses a non-open-ocean sample.
