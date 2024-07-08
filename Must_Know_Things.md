## Setting up reference images
* Switch to **Top** Orthographic view.
* Add **Image->Reference**. The reference image is added.
* Now you can tweak other settings of the image for better workings.
* Go to **Object Data Properties**.
* Enable Show in only **Orthographic** rather than both.
* Change **Side**, **Depth** for better workflow.
* Enable **Opacity** and change values according to need.


## Having extra **Objects** in Add
* Go to **Edit->Preferences**
* Search for **Add Extra Meshes** in **Add-ons** 
* Then go through these and **Enable** one by one of the need. 


## Link or Append
When you add an object from another blender file using,  
* **Link**: The object is not editable. You have to use this one as it is. 
* **Append**: The full control of the object is to you. You can change the object as you want.
* When you create an object with multiple meshes, then **Parent** all the meshes to one **Base** mesh and move it to a particular **Collection**.
* Then while **Appending**, import the particular **Collection** to the scene in need.


## Looptools
* Go to **Edit->Preferences->Add-ons**. Search for **Looptools** and enable it.
* Now you can use this tool by selecting **faces**, **right click** on it and go to **Looptools**.
* **Flatten** interpolates the positions, rotations of the vertices and flatten them for better look.


## Changing Material Preview Settings
* Go to **Shading** in top right panel.
* Click on the **Sphere** shape with shading.
* There are different **HDR** settings to use according to scene requirements.
* If you apply **Sunlight.exr**, then you can find objects with better shades.


## Selection
* If you import object from a file and there are multiple seperate objects within one, then go to **Edit->Face** mode, place the cursor on the object and press **L** to select the object.


## Search
* If there are many objects in the **Scene Collection**, then don't forget to use the **Search bar** above. 


## Random
* Always apply **Scale** using **Ctrl+A** after scaling the object on desired size to get global transformations.
* Always recalculate normals using **Shift+N**.
* Always press **S** for even extruding while **Extrusion**. 
* To use **Checker Disselect** from **Select**, at first select a **loop of faces** pressing **Alt**.
* You can have multiple windows in blender. Just use this one for better workplace. 


## Smooth Shading
* It takes 2 faces and blends them. Like this there are many types of calculations going on to perform shading. It doesn't know the difference between the numberous number of faint lines and the angle 90" between edges. It treats this as flat lines. 
* We need to force blender to know that when something is at certain angle, it should not be smoothen and should be treated as hard edge there.


## Edge Creasing
* It's used to make the edge sharper while using suvb-division surface modifier.
* It has a factor of 0 to 1. **Selecting object+Shift+E**
* We dn't get control of the edge then. Instead of using it we can use loop cut to perform beveling. That's more handy to do.

