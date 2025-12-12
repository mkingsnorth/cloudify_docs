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


`Cloudify <https://blendermarket.com/products/cloudify/?ref=361>`_ is a Geometry Nodes–based volumetric modifier for Blender 5.0 and later.
It converts closed (watertight) meshes into controllable volumetric clouds using
Blender’s new Grid and Volume Displacement systems.

This project is intended for **experienced Blender users** who want fine-grained
control over volumetric effects or who wish to study and adapt modern grid-based
volume workflows. Cloudify is provided as a fully editable demonstration setup,
not as a one-click “make clouds” solution.

.. image:: /_static/car.jpg
   :alt: Cloudify Logo
   :align: center

.. raw:: html

    <br><br>


Purpose and Scope
-----------------

Cloudify serves two primary purposes:

- As a practical tool for generating procedural volumetric clouds and effects
- As a reference implementation demonstrating Blender 5’s Grid architecture

Users are encouraged to explore the node tree, modify it, and repurpose parts of
the system in their own projects.

What Cloudify Is
----------------

Cloudify is:

- A non-destructive modifier-style Geometry Nodes setup
- Fully procedural and parameter-driven
- Compatible with standard modifier stacks
- Capable of exporting OpenVDB volumes
- Designed for experimentation, learning, and production workflows

What Cloudify Is Not
--------------------

Cloudify is not:

- A beginner-friendly volumetric preset
- A real-time cloud simulation system
- Optimised for low-spec hardware
- Intended to hide Blender’s volumetric complexity

Users unfamiliar with Geometry Nodes or volumetric concepts are strongly
encouraged to watch the accompanying :ref:`tutorial video <tut_vis>` and :ref:`volume displacement video <how_it_works>` before diving in.

Requirements
------------

Cloudify requires:

- Blender 5.0 or later
- Cycles renderer (recommended)
- A system capable of handling volumetric grids


.. _tut_vis:

Watch the Tutorial
--------------------------------------

To understand how Cloudify works and get the most out of it, check out the **YouTube walkthrough**
explaining the setup and workflow behind this modifier.

|intro_video|

.. |intro_video| raw:: html

    <iframe width="560" height="315" src="https://www.youtube.com/embed/1wtgED5sqFs?si=8T2wnpaGgRkiVZNW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

.. _how_it_works:

Volume Displacement Video
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
   Troubleshooting <troubleshooting>
   contact