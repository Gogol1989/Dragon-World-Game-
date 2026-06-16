Cloud shadow fix - shader decal v4

Changes made:
- Cloud shadows now use the same reliable Earth-material decal strategy used by the dragon shadow fallback.
- The old transparent tangent plane cloud-shadow meshes are hidden and kept only as data containers for wind drift, size, and strength.
- Each frame, cloud shadow directions are updated in shader uniforms, and the Earth fragment shader darkens the actual globe surface by angular distance from each cloud bank.
- This prevents cloud shadows from appearing on the bottom/back surface of cloud sphere puffs or disappearing behind globe/water/lake layers.
- Cloud shadows now render after lake/ocean/land color composition and before the final dragon shadow decal, so they remain visible across ocean, land, and lakes.

Main edited file:
- cinematic_earth.html

Key implementation points:
- MAX_CLOUD_SHADER_SHADOWS = 96
- New Earth uniforms: cloudShadowCount, cloudShadowDirs, cloudShadowSizes, cloudShadowStrengths
- New fragment shader block: FINAL CLOUD SHADOW DECALS
- Updated updateClouds() to feed cloud shadow decal positions to the Earth shader.
