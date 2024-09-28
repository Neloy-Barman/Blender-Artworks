# Hard Surface Modeling

There is a free course for modeling realistic and cool things. Find it <a href="https://www.blenderbros.com/jumpstart">here</a>. Just create an account there and move accordingly with the video. You will get the video link for the course within the mail.

## Course Content Link
* <a href="https://www.blenderbros.com/products/hard-surface-modeling-jumpstart?cid=252d30ad-ca7e-457c-b259-9a97bc6be5a9"></a>



* Go to Viewport Shading from upper panel. Enable **Cavity** to get a clear view of the sharp edges.
* We can enable **Shadow** also for proper view purpose. But it may cause performance issues for the hardware things. 
* Enable **Face Orientation** to get to know the inside and outside faces.      
* Click on **Status Bar** and enable **Scene Statistics**. It will show counts of verts, faces and others. 


## Things to keep in mind
* It's better to work in side-view. Go to the **Right** view from the pie menu. Then the side view hits the Y-axis perpendicularly. Lot of tools such as hard-ops works better in the Y-axis. So, it's recommended to use **Right** view as the side-view to start modeling. 
* Whenver we scale something on any axis, we always need to reset scaling to 1 using **Ctrl+A**. Otherwise problems get created when applying beveling because the scaling gets off-balanced.
* If use add-ons like **Box-cutter**, it adds scale reset automatically when we start using cutters and we don't have to reset manually. 
* When we work with the orthographic view, we don't need to specify the axis, it's rotated along the axis we are looking at.





* When we want to create a cut on the object of a particular shape, we will select the cutter shape and the object pressing **Shift**. Then press **Ctrl+-** to apply bool tool and cut the object. It applies the boolean modifier automatically. To use this we have to enable the **Bool Tool** add-on from preferences.  
* The object we use as cutters can be moved to seperate collection, so that when the work is done we can turn them off for hassle free work.  

* It's a better habit to create bevel with even number of segments. It's because if we create a lower poly version of the object, we will make bevels less dense. So, that we can select every second edge of the bevel and dissolve them. This will cut the resolution of the bevel in half. 
* If we use odd number, then we may have to remove an edge that holds the flatness of the bevel. But we don't want to disturb the outer edges. 
* Before we cut anything, we need to smooth out the mesh. Perform auto-smooth, which smoothens certain angles and others. We have to do this for every object.
* Don't move beveled cutter to that much deep that intersects with edge that will be or is beveled. So, we want to avoid overlapping of bevels. It's possible but it requires a lot of working in terms of topology fixing. 
* Before symmetrizing, we need to reset the rotation and we can do it by pressing **Ctrl+A** and select **Rotation**.


## Shading problem and potential fixes
* When there are a number of faces and these get cut and turned into angles, then there arises some shading problem.
* There will be a lot of vertices and edges within n-gons behaving weiredly. So, we have to fix this.
* Fixes: -
    * **Loop Cuts**: - We need to add a number of loops both in the cutter and to get cut objects that will maintain the shading within the object. Make sure that the ingoing loops kinds of encompass the structural edges. The loop should not be falling on the edge.   
    * **Knife Tool**: - We can add a edge using knife to create a tight shading and it will isolate problematic area. 
    * **Inset**: - Insetting faces will add a security parameter to the shading. It will isolate the middle shade from the outer one.
* No matter how much you try, you will never have a perfect shading. 
* When we will have a lot of loop cuts in the object, then there will be less shading distortions.  
* When we join objects using booleans on steep surfaces, then there of course will be a lot of distortions. We have to fix them mannually looking at them.
* We should add a lot of loop cuts in both the objects.
* We need to follow the order of the topology flows, how these loops are flown within. We need to provide a parameter loop within the mesh using **Knife** tool so that the shading flow is kept untouched.  
* We always need to find the shading break within the mesh and fix it.    


## Booleans in steeper faces
Whenever we have edges in the steep angle, it's generally a bad idea to bevel edges on them.
* The beveling gets pulled very badly and it breaks the shape.
* So, whenever we have booleans connecting to main mesh, we need to make sure that the connections are more or less 90 degrees towards the edge that's gonna get beveled.

## Cleaning Up meshs
* **Machine3Tools** CleanUp: - Select the mesh and press **3**.
* Go to 3D print ToolBox -> Clean Up -> Make Manifold.
* HardOps -> Operations -> Clean Mesh