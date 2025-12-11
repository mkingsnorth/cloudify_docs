VDB Export
=============================================  

The Cloudify setup includes a **Bake node**, allowing you to export the generated volume grid to a standard
``.vdb`` file for use in other software (Houdini, Unreal Engine, Blender projects, etc.).

How to Bake
-----------

1. In the Geometry Nodes Editor, locate the **Bake node** near the end of the Cloudify node chain.  
2. Choose **Still** for a single-frame bake, or **Animation** to export a sequence.  
3. Under **Bake Target**, select **Disk** and click **Custom Path**.  
4. Choose an output folder where you want the ``.vdb`` file saved.  
5. Press **Bake**.

Blender will generate the volume and save the result as an OpenVDB file.

Tips:

- For heavy or high-resolution grids, baking may take a while — progress is shown in Blender’s status bar.
- Once baked, you can import the ``.vdb`` back into Blender via  
  :menuselection:`Add --> Volume --> Import OpenVDB`.
- This is useful for archiving, rendering in other scenes, or sharing results without re-evaluating the node tree.