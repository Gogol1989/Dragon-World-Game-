NASA tiled base map update

This build uses the uploaded NASA Blue Marble tile set as the primary Earth base-color source.

Tile layout used in the shader:
Top row:    A1  B1  C1  D1
Bottom row: A2  B2  C2  D2

The older assets/base.jpg remains as a fallback global texture. The shader samples the correct tile from UV space rather than stitching all tiles into one giant image. This keeps the architecture ready for higher-resolution tile streaming later.

Seb-style spherical height-derived terrain normals, lakes, ocean normals, dolphins, fire flipbooks, and other previous effects are preserved.
