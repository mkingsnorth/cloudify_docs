Controls
=============================================  


The modifier exposes several useful controls for rendering volumetric clouds.

**Voxel Size**  
   Controls the resolution of the generated grid.  
   Smaller = higher detail but slower performance.  
   Typical range: **0.01 – 0.3 m**.

**Density**  
   Multiplies the grid’s density field to control the opacity of the cloud.  
   Higher values = thicker cloud.

**Gradient Width**  
   Controls falloff at the edge of the volume for a softer silhouette.

**Geometry Expand**  
   Expands the underlying geometry before voxelisation, allowing for more space around thin areas.

**Volume Expand**  
   Expands the volume grid boundary to prevent clipping during displacement.


Noise Controls
--------------

**Displacement Amount**  
   Controls how far voxels are displaced from their original positions.

**Proportions (X / Y / Z)**  
   Scales the displacement intensity independently per axis.

**Type**  
   Selects the noise basis: *Standard (Perlin-like)*, *Voronoi*, or *Custom*  
   (user-defined function in the node tree).

Vector Type (Gradient / Curl)
-----------------------------

This dropdown affects how the noise produces vector displacement:

- **Gradient** → uses standard gradient vectors from the Noise Texture  
  (smooth billowing movement; best for most cloud shapes)

- **Curl** → produces curl noise, generating swirling, vortex-like displacement  
  (useful for stylised clouds)

Curl mode is more dynamic but may be harder to control.

Standard Noise Controls
-----------------------

When the **Noise Type** is set to *Standard*, the modifier uses Blender’s built-in
**Noise Texture** node under the hood. This provides classic fractal noise suitable
for soft, organic cloud shapes. The following controls become available:

Seed
~~~~~~

Randomises the noise pattern without altering any other settings.  
Use different seeds to explore variations in the cloud’s internal structure while
preserving overall scale and behaviour.

Scale
~~~~~~~

Controls the base frequency of the noise field.

- Larger values → smaller, finer details  
- Smaller values → broader, smoother shapes

A typical working range is **0.05 – 1.0**, depending on desired visual complexity.

Detail
~~~~~~~

Determines how many fractal octaves (layers of noise) are added to the base noise.

- Low Detail → smooth, simple billows  
- High Detail → sharper, more intricate cloud texture

At very high voxel resolution, higher detail can significantly increase computation cost.

Roughness
~~~~~~~~~~~~~~

Controls the **weighting of the higher-frequency octaves** in the fractal noise.

- Low Roughness → each octave contributes less, producing gentle transitions  
- High Roughness → stronger contribution from fine details, creating a more turbulent look

This essentially governs how quickly details break down at smaller scales.

Lacunarity
~~~~~~~~~~~~~~

Sets the **frequency multiplier** between successive octaves.

- Values around **2.0** (Blender’s default) produce natural-looking fractal noise  
- Lower values reduce contrast between octaves  
- Higher values exaggerate the spacing of detail layers

This is a key parameter for shaping the “rhythm” or layering of cloud formations.

Distortion
~~~~~~~~~~~~~~

Applies a warping pass to the noise field, bending and stretching the pattern.

- Low Distortion → stable and voluminous cloud shapes  
- High Distortion → twisted, stormy, or chaotic structures

This is especially useful for adding motion or directional flow when animating clouds.

Voronoi Noise Controls
----------------------------

When the **Noise Type** is set to *Voronoi*, Cloudify uses Blender’s Voronoi Texture node
to generate cell-based patterns that are ideal for chunkier, broken cloud shapes.
Voronoi displacement can create dramatic, sculptural silhouettes or turbulent storm-like forms.

The following controls become available:

Seed
~~~~~~~

Randomises the underlying Voronoi pattern while keeping all scale and shape settings intact.
Changing the seed is the quickest way to explore alternate “cell” arrangements.

Scale
~~~~~~~

Controls the overall size of the Voronoi cells.

- Larger values → many small cells (high-frequency structure)  
- Smaller values → large, blocky clusters (broad cloud shapes)

Typical range: **0.5 – 3.0** for cloud-like structures.

Detail
~~~~~~~

Adds fractal layering on top of the base Voronoi pattern.

- Low Detail → clean geometric cells with soft displacement  
- High Detail → more complex breakup, cracking, and noisy surfaces

Useful for adding realism to storm clouds or highly eroded formations.

Roughness
~~~~~~~~~~~~~~

Controls the weight of high-frequency detail added to the Voronoi fractal layers.

- Low Roughness → smooth transitions between cells  
- High Roughness → sharper variations and a more chaotic, wind-torn look

Especially effective when used with Curl Vector Type for turbulent flow.

Lacunarity
~~~~~~~~~~~~~~

Adjusts the **frequency multiplier** between detail layers.

- Default **2.0** gives natural fractal spacing  
- Lower values → more uniform detail  
- Higher values → exaggerated differences between octaves

Lacunarity influences the “rhythm” of the Voronoi layering.

Smoothness
~~~~~~~~~~~~~~

Softens the sharp borders between Voronoi cells.

- Low Smoothness → crisp, cell-like divisions  
- Higher Smoothness → blurred transitions and more organic cloud structures

This is a key parameter for shifting Voronoi from “geometric” to “natural”.

Randomness
~~~~~~~~~~~~~~

Controls how irregular the cell shapes are.

- Low Randomness (near 0.0) → evenly spaced, grid-like patterns  
- High Randomness (0.8–1.0) → chaotic, broken cell structures  
- Values above 1.0 produce stretched and distorted cells

Useful for simulating fractured clouds, storm fronts, or magical effects.

Custom
----------------------------

This is intentionally left blank for you to build your own noise function using Blender's Geometry Nodes.  See the section on :ref:`customisation<customisation>`.



