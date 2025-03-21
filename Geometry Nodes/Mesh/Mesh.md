# Mesh


## Operations

### Dual Mesh
It takes every face and put a vertex in the middle position. Then create a new mesh connecting all of those vertices. We can take an icosphere and create a cool shield effect from it.
<img src="Operations/dual_mesh.png">

### Edge Paths to Curves
It converts the edge paths to curves. To make it work properly, we need a couple of more nodes.
<img src="Operations/edge_paths_to_curves.png">

### Edge Paths to Selection
We can convert the edge paths to a particular selection and use it for different purposes.
<img src="Operations/edge_paths_to_selection.png">

### Extrude Mesh
This takes all of our vertices and extrudes them. It's the same as we have in the edit mode. We can have a particular vertex group as selection and pass it here. We can also define random value for offset scale. We can define only edges or even vertices.  
<img src="Operations/extrude_mesh.png">
We can also define to extrude from side or top from the attributes in the node.
<img src="Operations/side_extrude.png">

### Flip Faces
A face has 2 sides. We can view this by enabling the face orientation. This node simply changes the face orientation. We may need this in any corner cases. We can also define a mask through the selection.
<img src="Operations/flip_faces.png">

### Mesh Boolean
We can use this to cut hole in with another object. We can also perform other tasks such as intersection and joining. Set the intersecting object position relative.
<img src="Operations/mesh_boolean.png">

### Mesh to Curve
It takes every edge and converts them into curves. Then we can create cool animation using this based on curves. We can use trim curve to trim curves changing the factor values.
<img src="Operations/mesh_to_curve.png">
Then we can again convert the curve to mesh and use it according to need.
<img src="Operations/mesh_to_curve_2.png">

### Mesh to Points
It takes a face and place a point in the middle of each face. It also takes vertices, edges and corners. Then place the points accordingly. We can change the radius of the points.
<img src="Operations/mesh_to_points.png">

### Mesh to Volume
It takes the original mesh and converts it into volume. We can also remesh it using 'Volume to Mesh'.
<img src="Operations/mesh_to_volume.png">

### Sample Nearest Surface
Is is similar as the 'Geometry Proximity' node. We can sample something from a different mesh. For example, position of a mesh. This node will sample the position from the mesh's nearest faces. It uses the nearest faces as the position. We can simply use it for any kind of attribute we want.
<img src="Operations/sample_nearest_surface.png">

### Sample UV Surface
Suppose, we want a similar displacement as some other mesh.
<img src="Operations/sample_nearest_surface.png">

### Scale Elements
We can scale the mesh using this. For example, we can make a cool effect. Let's take a icosphere and add a 'Dual Mesh' node. Then pass it through 'Split Edges'. It will split all the edges and those are not connected. Now if we apply the scale node, it will scale individual faces or edges whatever we select. We can also take a 'Noise Texture' and 'Color Ramp', then djust the scaling based on that.
<img src="Operations/scale_elements.png">

### Split Edges
It will split all the edges of the mesh.
<img src="Operations/scale_elements.png">

### Subdivide Mesh
It subdivides the mesh as we do in the edit mode. We can control the number of subdivisions we want. It doesn't change the shape of the object, but gives us much topology.
<img src="Operations/subdivide_mesh.png">

### Subdivision Surface
It smoothens out the object as we do in the subdivision surface modifier. We can control the level, edge crease and vertex cross here.
<img src="Operations/subdivision_surface.png">

### Triangulate 
It simply triangulate the faces. It converts every face into 2 triangle.
<img src="Operations/triangulate.png">


## Read
We can grab information about the mesh using this category nodes.

### Edge Angle
It gives a value for every single edge for how sharp the angle is there. We can use a 'Color Ramp' and 'Viewer' node to view this.
<img src="Read/edge_angle.png">

### Edge Neighbors
It outputs us the number of faces that uses the edges. For example, if we delete one face in an icosphere, there will be 3 single edges that are used by onlyt one face. Now if we use a 'Compare' node and set it to equal and then take a 'Mesh to Curve' node, then we want it to convert into a curve when the value is 1. Now we can join both the geometry using 'Join Geometry'. Then we can convert the curve again to mesh using 'Curve to Mesh' and using 'Curve Cycle' as the profile curve.
<img src="Read/edge_neighbors.png">


### Shortest Edge Paths
It calculates the shortest path from every vertices through the edges of our mesh to our set end vertices. We have to define the end vertex. We need to assign vertex groups as the attributes to work with this. When we provide the start and end vertices, it will provide us with the shortest path edge. This one by default takes all the edge cost as 1. To change it we can use Random Value or Noise Texture for varying costs for different edges. 
<img src="Read/shortest_edge_paths.png">
Normally we use Edge length for edge cost, because the longer the edge, the more cost it should have. For that, we will use Edge Vertices and Vector Math node with Distance for the calculation. In this way, the shorter edges have more weight than the shorter ones. 
<img src="Read/edge_vertices.png">
