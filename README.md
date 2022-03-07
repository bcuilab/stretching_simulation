# stretching_simulation

The Python jupyter notebook (.ipynb) requires to have the Fenics package installed (https://fenicsproject.org/download/).

The script loads the mesh (.xml), scales it to the correct size, and applies a homogeneous pull to each sides in order to achieve 50% elongation in every dimension.
You can adapt this to your own mesh. Here, the boundary conditions here expect a rectangular mesh. This can be adapted to any shape provided you can define the boundary conditions correctly, or load a mesh with boundary markings (from GMSH for example). 

Three .pvd files are produced for the displacement, strain and stress. Download paraview (https://www.paraview.org/download/) to visualize them. 

To reproduce figure plots in paraview, follow these steps:
1. Load in displacement.pvd
2. Load in stress (strain).pvd
3. Select both in the left dropdown bar with the control button
4. Add a 'Append Attributes' filter. 'Apply', in the left drop down, the lowest 'Appended Attribute' data object.
5. Apply 'Warp by Vector' filter to the lowest data object in the left bar (appended attribute)
6. In the coloring (left drop-down), select stress (strain) and color by magnitude.
