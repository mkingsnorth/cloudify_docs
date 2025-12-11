.. _customisation:

Customise
==================

It is highly recommended that you explore altering the noise setup to get different displacement effects.

First, select 'Custom' in the Cloudify modifier's 'Type' dropdown.

.. image:: /_static/modifier_custom_setting.png
   :alt: Custom Noise Type Example
   :width: 90%
   :align: center

The modifier uses Blender 5’s new Closure system so you can add new noise types.  Here is the node tree set up used in Cloudify as seen from the Geometry Nodes editor:

.. image:: /_static/cloudify_noise_setup.png
   :alt: Noise Setup Example
   :width: 90%
   :align: center

To make the set up editable, in the Geometry Nodes editor, select the Cloudify modifier and click the package icon:

.. image:: /_static/make_editable.png
   :alt: Make Editable Example
   :width: 90%
   :align: center

At the bottom of the node tree, you can add a new noise displacement by adding a calculation to the existing position of each voxel.

.. image:: /_static/add_new_type.png
   :alt: Custom Noise Node Example
   :width: 90%
   :align: center

For instance, remove the multiply node and add a new noise texture node to create a different noise basis for pushing and pulling the incoming positions.

.. image:: /_static/new_noise_type.png
   :alt: New Noise Type Example
   :width: 90%
   :align: center

You could then, for example, layer the effect by adding another noise node and add it to the sclae parameter of the first noise node:

.. image:: /_static/layered_noise.png
   :alt: Layered Noise Example
   :width: 90%
   :align: center

See the `free tutorial video <https://youtu.be/fPFsNWzlxzk>`_ which explains the concept behind Cloudify, and feel free to ask if you have questions by contacting `info@configurate.net <mailto:info@configurate.net>`_.

