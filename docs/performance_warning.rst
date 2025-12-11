Performance Warning
=============================

.. image:: /_static/performance_issues.png
   :alt: Performance Warning
   :align: center

Cloudify is not for the faint-hearted!  Volume displacement is **extremely** memory and processor intensive.

It’s intended for users who want to dig deeper into Blender’s new Grid and Volume Displacement systems.
👉 It’s strongly recommended you watch the companion tutorial video first to understand how it works.

System Requirements
-----------------------------

* Intel i7 / AMD Ryzen 7 (or better) CPU
* 32 GB RAM minimum (64 GB+ recommended for complex scenes)
* Dedicated GPU with at least 8 GB VRAM (NVIDIA RTX series recommended)

The included examples use a **larger Voxel Size** in the Cloudify modifier to prevent Blender from crashing when
the files load. Lower voxel sizes will create slower grids.

You *can* experiment with increasing detail by reducing the voxel size —  
but proceed carefully: smaller values have a **huge** impact on performance, even on high-end PCs.
