Getting Started
=============================================  

This section gives you a practical overview of how to begin using the Cloudify modifier.

1. Select an Object
---------------------

.. image:: /_static/select_object.png
   :alt: Starting Object Example
   :width: 90%
   :align: center

Cloudify works best on **watertight meshes** (objects with no holes or open surfaces).  
Good starting shapes include:

- UV Sphere
- Cube
- Remeshed characters or props
- Any closed mesh from your modelling workflow

2. Apply Scale
--------------

.. image:: /_static/apply_scale.jpg
   :alt: Apply Scale Example
   :width: 90%
   :align: center

For Cloudify to behave predictably, make sure the object is correctly scaled:

.. code-block:: none

   Ctrl + A → Apply Scale

A typical recommended object size is **2–10 metres** across for default Cloudify settings.

3. Add the Cloudify Modifier
----------------------------

Once you have :ref:`installed<installation>` the modifier asset, there are two ways to add the modifier:

- Go to the :guilabel:`Modifiers` panel on the right hand side and click :guilabel:`Add Modifier` → find *Cloudify* in the *Generate* category.

.. image:: /_static/add_modifier_panel.jpg
   :alt: Add Cloudify Modifier
   :width: 90%
   :align: center


- **Drag–drop the Cloudify Asset** from the Asset Browser onto your object,

.. image:: /_static/add_modifier_asset.jpg
   :alt: Cloudify Asset Browser
   :width: 90%
   :align: center

Once added, Blender converts your mesh into a **volumetric grid** and applies layered noise displacement.

.. image:: /_static/modifier_added.jpg
   :alt: Initial Cloud Example
   :width: 90%
   :align: center

4. Set up a Rendered View
--------------------------

.. image:: /_static/rendered_view.png
   :alt: Rendered View Example
   :width: 90%
   :align: center

Cloudify is a volumetric effect, so for best results:

- Switch the viewport to :guilabel:`Rendered` mode.  
- Use **Cycles** for final-quality volumetrics.  
- Add a Sky Texture in the World settings for better lighting.  Good lighting is key to showing off the volume:

.. image:: /_static/sky_texture_node.png
   :alt: World Sky Texture
   :width: 90%
   :align: center

- Eevee works, but may show lower detail.
  

5. Adjust the Voxel Size
------------------------

.. image:: /_static/voxel_size.jpg
   :alt: Voxel Size Example
   :width: 90%
   :align: center

A key setting is the **Voxel Size**, which controls the detail of in volume.

- Large values → fast but low detail  
- Small values → high detail but slow and memory-intensive

Typical working values:

- Preview: **0.1 – 0.3 m**
- High detail (fast GPUs): **0.01 – 0.05 m**

Start large, then refine as needed.

.. tip::

   Although decreasing the voxel size usually increases detail, many cloud like forms do not require high amounts of detail to look good. Experiment with different sizes to find a good balance between performance and appearance.

6. Shape the Cloud
------------------

.. image:: /_static/shape_cloud.png
   :alt: Cloud Controls Example
   :width: 90%
   :align: center

Experiment with these core controls:

- **Density** – Makes the cloud thicker or more transparent.  
- **Gradient Width** – Softens or sharpens the cloud silhouette.  
- **Geometry Expand** – Adds buffer space before voxelisation to avoid clipping.  
- **Volume Expand** – Enlarges the voxel grid when displacement pushes the cloud outward.

For creative shaping, explore:

- **Displacement Amount**  
- **Noise Type** (Standard, Voronoi, Custom)  
- **Proportions (X/Y/Z)** for directional stretching
