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