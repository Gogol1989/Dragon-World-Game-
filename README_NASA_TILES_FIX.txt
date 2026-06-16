NASA tiled base map update - WebGL texture unit fix

The earlier shader loaded all 8 NASA tiles as separate sampler2D uniforms, which exceeded MAX_TEXTURE_IMAGE_UNITS(16) on many browsers/GPUs and caused Earth not to render.

This build keeps the NASA tile quality but packs A1/A2/B1/B2/C1/C2/D1/D2 into one 8192x4096 atlas:
assets/nasa_tiles/world_atlas_8k.jpg

The shader now samples this single atlas via nasaAtlas, reducing terrain fragment shader texture usage below the WebGL limit.
