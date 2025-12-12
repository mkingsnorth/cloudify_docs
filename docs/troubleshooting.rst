.. _troubleshooting:

Tips and Troubleshooting
==============================================

This section collects practical advice, common issues, and performance guidance
for working with Cloudify. Cloudify is a volumetric, grid-based Geometry Nodes
setup and is intended for experienced Blender users working with Blender 5.0+.

.. note::
    
    If you are having any issues do not hesitate to :ref:`Contact Us <contact>`

System Requirements
-------------------

Cloudify relies on Blender’s new Grid and Volume Displacement systems and performs
dense volumetric calculations. For the best experience, the following system
specifications are recommended:

- Blender 5.0 or later
- 32 GB or more RAM
- Dedicated GPU (NVIDIA RTX-class preferred)
- Cycles renderer

Lower-spec systems can still open and modify the files, but may experience slower
viewport performance, longer bake times, or instability when working with small
voxel sizes.

Mesh Requirements
-------------------

Cloudify generates volume from the interior of a mesh. For predictable results:

- Use watertight (closed) meshes
- Avoid thin, single-surface geometry
- Apply scale before adding Cloudify (``Ctrl + A > Scale``)
- If necessary, add a Remesh Modifier before Cloudify

Objects that are not watertight may produce missing or irregular density.

Scene Scale
----------------------

Cloudify is sensitive to object scale. For best results:

- Scale objects to approximately 2–10 metres
- Apply scale before adjusting voxel size
- Avoid working with very small objects

Incorrect scale is one of the most common causes of poor results.

Performance Tips
---------------------------

If Cloudify feels slow or unresponsive:

- Increase voxel size (this has the largest performance impact)
- Reduce noise detail or displacement strength
- Work at higher voxel sizes while shaping, then refine later
- Use Cycles with viewport denoising enabled
- Avoid extremely dense grids during look development

Small reductions in voxel resolution can result in significant performance gains.

Blocky or Low-Quality Volumes
----------------------------------------

If the volume appears blocky or coarse:

- Decrease voxel size gradually
- Check that the object scale is correct
- Reduce excessive displacement strength
- Increase noise scale if patterns appear too tight

Voxel size should be adjusted before modifying other parameters.

Irregular or Missing Density
---------------------------------------

If parts of the volume are missing or uneven:

- Ensure the mesh is watertight
- Increase base density
- Reduce displacement amplitude
- Check that the object scale is applied
- Reset the noise seed if artifacts appear

Many density issues are caused by extreme parameter values rather than errors.

Volume Disappears When Adjusting Settings
----------------------------------------------------

If the volume vanishes after tweaking parameters:

- Density values may be too low
- Displacement may be pushing voxels outside the mesh bounds
- The object may be too small in scene scale

Try increasing base density, reducing displacement strength, and confirming
object scale.

Animation Considerations
-----------------------------------

All Cloudify parameters can be animated. For complex or heavy animations:

- Preview at higher voxel sizes
- Bake the volume to VDB for final output
- Avoid animating voxel size directly

Baking to VDB is strongly recommended for long or complex animations.

VDB Export
---------------------

Cloudify includes a Bake node for exporting volumes as OpenVDB files. Exported
VDBs can be used in:

- Blender Volume Objects
- Houdini
- Unreal Engine
- Other VFX or compositing tools supporting OpenVDB

Baking converts the procedural setup into a static or animated volume for
improved playback and rendering performance.

Best Practices Summary
---------------------------------

- Apply scale before use
- Start with larger voxel sizes
- Adjust voxel size before tuning noise
- Work in rendered view to evaluate density
- Use Remesh for problematic meshes
- Bake to VDB for final output

Support
------------------

If you encounter issues not covered here or have questions about the setup, :ref:`please get in touch <contact>`.

Feedback and suggestions are always welcome.
