
# Node Wrangler
* Preview Node: - It plugs the node to the output viewing node so that we can view how the node final result looks like.




# Nodes

## Shader Nodes
All the shader nodes have the green tab to identify. These are the real-life material means what the object is actually made of.
* **Emission: -** It emits light. When we need to glow something, we use this one. Example cases can be light bulb, sun object or glowing lava. Increasing the **Strength** value makes the emission brighter.
* **Principled BSDF: -** We can make a tons of materials with it. It's basically the master node.


## Texture Nodes
All the texture nodes have orange color tab to identify. 

### Noise Texture 
This is the most common one that we will use. It adds some noise.
* **Scale:** Increasing scale value will more noise.
* **Detail:** Increasing this will add more detail.
* **Roughness:** Decreasing this will make the mesh blobby. Increased value will add more details.
* **Distortion:** This will make the texture distorted.

We can add the output of the texture node **Fac** to the input of the principled BSDF shader **Base Color** node. This Fac is black and white. There is also **Color** output node and it just adds some random colors. Mostly **Fac** is preferable.

### Wave Texture 
We can change in between Wave Type, Band Direction and Wave Profile to get different kinds of textures. There are also other settings to work on and change it.

### Voronoi Texture
We can change Dimensions, Feature Output and Distance Metric as well as other settings to get different kinds of design. 

### Checker Texture
If we want to have checker board design on something, we can use it. Also we can change Color1 and Color2 to get board of different ones. 

### Brick Texture
It is used to create brick or tiles on a mesh.

### Musgrave Texture
It is also a kind of noise texture.

### Magic Texture
It provides random design with colors on the mesh.


## Nodes according to Colors
* **Yellow**: Color Data
* **Grey**: Black and White Data
* **Purple**: Vector or Normal Data
* **Green**: Shader Data

If we connect nodes of different colors, then we will have unexpected behaviours. 



