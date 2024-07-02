# Shading
* Go to **Shading** from the top panel.
* From the right top panel, go to **Viewport Shading**, enable **Scene Lights**.
* You can choose any **HDR** option to suit the best one according to you. 
* Rotate the scene to get better lighting and the shadows of the objects.
* Adding **Material** to the object will create a node in the lower panel. This node represents the material properties. whatever we do in the materials can be done easily within the nodes also.
* We can also add new nodes by pressing **Shift+A** in the lower panel and choose the desired node.
* To connect nodes, select the nodes pressing **Shift** and press **F**. The nodes are connected then.
* Principal BSDf -> Principal Bi-directional Scalaring Distributional Function. It's a mathmatical algorithm to caculate light emission in the shader. Bi-directional means it deals with both reflected and absorbed light.

## Collecting Textures
* As a beginner, go to [Textures.one](https://3dassets.one/?q=&sort=popular) and search for textures according to need.
* Now download the zip file of 1k-8k according to need. If you are working with a more detailed and realistic textures, then download the files with higher resolution. Else lower ones will work properly.
* Make sure the downloaded file has these 3 different images **Normal, Roughness & Color maps**. These confirm something called **PBR->Physically Based Rendering**. These 3 basic maps are always needed. Sometimes there can be more of them.
* PBR is a set of rules that principal BSDF shader confronts to as well. How to interpret the light on the surface, how to do all of the things such as roughness, bumps with the normal mapping are set by this set of rules.   
* There is another map called **Displacement**. This is too heavy and an advanced topic. So, leave that.


## Applying Textures
* Go to **Shading**.
* If you are on the wrong drive, then extend the **>** arrow to right and go to the desired folder.
* Import the **Textures** from left side panel file browser. Drag them to the panel containing nodes.
* Apply **Materials** to the object.
* Connect the **Base Texture Color Node** to **Materials Base Color Node**. Now the applied texture can be seen. But the texture doesn't look very well.
* Connect the **Roughness Texture Color Node** to **Materials Roughness Node**. Before connection make the Color Space to **Non-Color**, as we will be using only the roughness.
* Import **Normal** texture to the **Nodes** panel. Switch to the **Non-Color**. Add a **Normal Map** node and connect it with the **Normal** image. Then connect the **Normal Map Normal Node** to the **Materials Normal Node**. 
* Sometimes we see a little streches on the rotation of the faces while working. This is because the sub-surface modifier. The UV Mapping is applied before the geometry is subdivided. So sometimes we need to add more geometries there to get rid of the streches but it dissolves our desired shape of the geometry.


## UV Mapping
* UV Mapping is a 2D interpretation of the texture to the 3D plane.
* There are many options how to make UV mapping. The quickest way is to use blender's smart algorithm.
* In the **Shading** window, selecting the object go to **Edit** moode pressing **Tab**. Then click on the **UV** from the top panel, then click **Smart UV Project** and confirm. This also can be invoked by pressing **U** and allowing the sub-processes.
* Now to see how the texture is projected, go to **UV Editing** panel from top, now selecting the **object**, you can see the texture projection. 
* **Smart UV Project** is an autmated projection and sometimes it's good to move with this one.    
* If you view the zoomed version of **Normal Texture** image in the **UV Editing** map, then you can see the x,y and z values of the rotations of the normals as color pixel values. Every pixel here is a different represention of its own normal.   
* In the left panel, you can do everything with the texture you want. You can **Scale, Rotate or Move Vertices, Edges, Faces or Islands** according to need by selecting the whole object or particular portions in the **Edit** mode.
* You can also do this in **Shading** panel by adding an **Input->Texture Coordinate->UV Node** and connect it to the **Vector->Mapping->Vector Node**. Now connect the **Mapping->Vector Node** output node to the **Base Texture->Vector** input node. Here you can perform all the transformations(Scale, Rotate, Move) on the textures.  


## List of websites that offers free PBR textures
* The websites can be found [here](https://gist.github.com/mauricesvay/1330cc530f6ab2ef33eb6a5ea56ef5bd).