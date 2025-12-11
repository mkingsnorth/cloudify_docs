Cloudify
=====================================


What is Cloudify?
----------------------------------------------

.. note::

   Blender 5+ only!


.. image:: /_static/cloudify_splash.jpg
   :alt: Cloudify Logo
   :align: center
   :width: 600px

.. raw:: html

    <br><br>

`Cloudify <https://blendermarket.com/products/cloudify/?ref=361>`_ is a **Geometry Nodes–based modifier** that transforms any watertight 3D object
into a fully volumetric cloud right inside Blender 5. Good for creating cloud or snow-like
3D effects.

It's a demonstration setup showcasing Blender’s new **Grid system** — designed for you
to study, repurpose, or adapt for your own creative experiments.


.. image:: /_static/car.jpg
   :alt: Cloudify Logo
   :align: center

.. raw:: html

    <br><br>

Features
-------------

- **Non-destructive modifier:** Works like any other Blender modifier — mix it on top of
  Subdivision, Displace, Remesh, etc.

- **Procedural volume generation:** Converts meshes into density grids and displaces them using
  layered noise fields.

- **Fully editable:** Tweak voxel size, noise scale, and displacement strength for variations.

- **Example setups:** Use it as a learning resource or foundation for your own volumetric
  workflows.

- **VDB Export:** The node tree contains a “Bake” node for exporting the volume as a VDB.


Watch the Tutorial
--------------------------------------

To understand how Cloudify works and get the most out of it, check out the **YouTube walkthrough**
explaining the setup and workflow behind this modifier.

|intro_video|

.. |intro_video| raw:: html

    <iframe width="560" height="315" src="https://www.youtube.com/embed/1wtgED5sqFs?si=8T2wnpaGgRkiVZNW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

How it works Video
--------------------------------------

Link: `Free Tutorial Video <https://youtu.be/fPFsNWzlxzk>`_

**Watching this video is strongly recommended**, especially if you're new to Blender 5’s Grid and Volume Displacement system.  This explains the core concepts used in Cloudify.

The video covers:

- How Blender’s new Grid system enables controllable volumetric displacement.
- Step-by-step setup of volume displacement in geometry nodes.
- Tips for performance and rendering.


Feedback welcome!
-----------------

This is an experimental release showcasing the power of Blender 5’s new volume system — have fun exploring,
and feel free to share your results or suggestions.

Email **info@configurate.net** if you have any questions or issues.

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   installation
   performance_warning
   get_started
   Controls <controls>
   how_it_works
   customisation
   exporting
   contact