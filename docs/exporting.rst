VDB Export
=============================================  

The Cloudify setup includes a **Bake node**, allowing you to export the generated volume grid to a standard
``.vdb`` file for use in other software (Houdini, Unreal Engine, Blender projects, etc.).

How to Bake
-----------

.. image:: /_static/bake_node.png
   :alt: VDB Bake Node
   :width: 90%
   :align: center

1. In the Geometry Nodes Editor, locate the **Bake node** near the end of the Cloudify node chain.  
2. Press the n key for the left hand side properies panel, and select the *Node* tab to see the Bake options.
3. Choose **Still** for a single-frame bake, or **Animation** to export a sequence.  
4. Under **Bake Target**, select **Disk** and click **Custom Path**.  
5. Choose an output folder where you want the ``.vdb`` file saved.  
6. Press **Bake**.

Blender will generate the volume and save the result as an OpenVDB file. In the output folder, the VDB file is located in the *blobs* subfolder

Tips:

- For heavy or high-resolution grids, baking may take a while — progress is shown in Blender’s status bar.
- Once baked, you can import the ``.vdb`` back into Blender via  
  :menuselection:`Add --> Volume --> Import OpenVDB`.
- This is useful for archiving, rendering in other scenes, or sharing results without re-evaluating the node tree.