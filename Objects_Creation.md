# Different types of objects/ shapes Creation


## Stairs
### Normal Stairs
* Create the upper and lower step from a plane or anything like edge or vertices. 
* Then apply **Array Modifier** and adjust Factor X, Y, Z value according to need.
* Go to **Edit->Edges** mode and selecting all **Edges**, press **M** and merge **vertices**.
### Metalic Stairs
* Do the same things as the **Normal Stairs** procedures.
* Just apply **Loopcuts** or **Sub-divide** to the whole object.
* Then add **Wireframe** modifier to the whole object.


## Curved Objects
* Add **Object** and apply **Array Modifier** to it accordingly.
* Then add **Shift+A**->**Curve->Bazier Curve**. 
* Select the curve, rotate it to **-90** on the **Y-axis**. Make the curve stright.
* Place the **Endpoint** of the curve to the **top** of the object.
* Selecting the object, apply **Curve** modifier and peek the selected curve from there.    
* Now changing the curve point placements will change the object shape according to curvature.
* Make the object parent for the curve to move along with object.
* To this one as a single object, apply the modifiers and get rid of them. Now this can be edited as single object.


## Water 
To Create **Water**,
* Consturct the **Shape** for the water.
* **Sub-divide** or create a lots of **Loop-cuts** through the shape.
* Select all the **Vertices** from the shape and create a **Vertex Group** of them in the object data.
* **Triangulate** the shape.
* Go to object mode. Add **Displace modifier** and apply **Cloud** texture.
* Then **Tweak** the **Properties** according to need.


## Custom Geometry
* Create a **Plane**, **Merge** all the vertices into one.
* **Extrude** the **Vertex** according to the necessary shape.


## Particles
Particle systems work with 2 types of objects. These are: -
* **Particle**: This is the **Shape** that will be created in **Huge Numbers**.
* **Emitter**: **Geometry** from which we can create these particles in various numbers and various directions. 
How to create: - 
* Create a **Shape** that you want to put as a **Particle**.
* Create an **Emitter Shape** within which you want to put the **Particles**.  
* Selecting the **Emitter**, go to **Particle Properties**. 
* In **Emission**, set the **Frame Start** and **End** to **0**.
* Go to **Render**, select **Object** and in object, select the **Instance Object** for the particular object.
* **Tweak** other properties such as **Rotation**, **Scale** to get better results.


## Pipes
* Create the **Shape** of the pipe using **Custom Geometry** process.
* Then convert it to a curve using **Object->Curve**.
* In **Object Data Properties**, go to **Geometry->Bevel** and change properties according to need.


## Tins
* Take a plane of **desired size**.
* Add a number of **Loop Cuts** on the desired direction.
* **Bevel** the loop cuts to even numbers more likely starting from 4 to any even numbers.
* Selecting the beveling faces, switch to **Face** select, press **Ctrl+-** to contradict selection.
* Now move the selected faces to **Z-axis**, and the **Tin** is ready. 


## Neon Lights
* Duplicate the **Edges** of the **Area** from the object and seperate them as a single object.
* Selecting vertices, apply **Skin** modifier and change the size according to need pressing **Ctrl+A**.


## Propellers
* Create a **circle**, **inset** the face for middlebase of the fan. 


## Texts
* **Shift+A->Text**.
* Selecting the text in **Object** mode, go to **Object Data Properties** to tweak with the properties.
* In **Edit** mode, you can change the text of the object.
* To center the text, in the object data properties, go to **Paragraph->Alignments** and make **Horizontal**, **Vertical** **Center**.
* To change the font style, from **Font**, select regular weight and select particular **.ttf** file. You can use your chosen ones by downloading them from **google fonts** and placing the **ttf** file there.
* To make the text **extruded**, go to **Geometry->Extrude** and change the value according to need. For **Bevel**, the settings is also in the **Geometry**. 


## Grease Pencil objects
* Add a **Grease Pencil->Blank** object using **Shift+A**.
* Then switch to **Draw** mode from **Object**.
* Drawing freely will make the art scattered in the viewport.
* But if you want it to be particularly on some plane. Then create a plane joining the objects.
* Switch the **Stroke Placement** to **Surface** and make the **Offset** 0.
* Adjust **Stroke** strength, **Radius** value to need.
* There are different types of styles in the left side panel in **Draw** mode, such as **Arc**, **Polyline**, **Curve** and many more.
* After creating an art, press **Enter** to place the object.
* Now selecting the pencil strokes, go to **Object** mode, **Object** and convert to **Bazier Curve**. Another object will be created. 
* Enable **Simplify Curves** add-ons from preferences. 
* Now selecting the pencil and new object layer, using **Shift+A**, add **Curve->Curve Simplify**. Adjust **Error** value from Distance Error.
* These **New Simplified Curves** can be adjusted accorrding to need in the **Edit** Mode.
* Then going to **Object Data Properties** go to **Bevel** and adjust depth and resoultion for better look.
* We can create wires or wire-like things for example using this methodology.


## Fog Effect
* Add a **Cube**, make it larger to match the **Fog** area.
* Selecting the **Object**, go to **Material Properties**, create a new **Material**.
* From **Surface**, **Remove** the shader.
* Go to  **Volume**, apply **Volume Scatter**.
* Now change the **Density** value according to satisfaction.
* Change **Color**.  


## Smooth Surfaes
If you want to create smooth surfaces, then you have to enable smooth shading.
* In **Object** mode, **Right click** on the object, then **Smooth Shade**. The smoothing algorithm tries to interpolate between phases and performs some smooth transition.
* Apply **Subdivision Surface** modifier.
* Go to **Viewport Shading**, Enable **Metcap Lighting** and select **Metal_Carpaint** to find the proper view of smooth surface shading. This will help to find out mistakes and do corrections based on them.
* Add more and more loopcuts close the the edge to get smoother and sharper edges. 
* To make realistic objects such as chairs, tables and some household tools, these smooth surfaces are needed. They reflect shading of lights.
* If you make one with hard surface modeling, then it's too tough to manipulate again.
* We can also use **Bevel** for low poly models as well as combine it with this modifier to get the best look.
* If we don't want the complexity of the geometry too much or low poly flat shading, then we can apply **Edge Split** modifier after applying **Beveling**.
* Working with these sometime is too tricky, always perform **Test and Trial** before reaching to the final look.
* The smoothing will work and look the best when the topology has a number of sub-divisions.
### When to use what
#### Combining Edge split and Subdivision Surface modifier
* If you **Bevel** edges and you don't want to show the beveling angles, then apply **Edge Split** modifier, change **Edge Angle** to look for the better result. 
* Now looking from above some beveling elements may still be shown, so, now apply **Subdivision Surface** modifier to get rid of this problem. Change **Levels** to get a better result.
#### Combining Bevel, Edge Split and Subdivision Surface modifier
* If you also want smooth shading on the beveling cornered object, then apply **Bevel** modifier. Tweak values.
* Then Follow the previous methods from the above procedures.
### Objects without Boolean modifiers
* When you need to smoothen object, you can't use boolean modifier. That will make the object more complex.
* In those cases for circle, or other types of meshes within objects, use **Looptools** add-ons features.
* Then apply modifiers to get better results.


## Object Creation using Spin
* Create the basic shape using **Single Vert**.
* Then going to **Edit** mode, Find **Spin** from left Side panel.
* Now applying spinning, tweak the properties and test with them to get the better results.
* Use them for the desired shaped object.


### Tree Tob
* To add a pre-generated tree branches, **Shift+A->Curves->Sapling Tree Gen**.
* Change **Branch Distribution, Branch Rings and Random Seed** values to get a desired shape.
* Enable **Show Leaves** for the leaves.
* Go to **Branch Distribution** and tweak settings there to change angle or other things.
* Create a tree tob using **Screw** modifier.
* To create **Mud** within **tob**, duplicate the tob and apply **Screw** modifier. Then join the top vertices to create a face. Now move or scale vertices to get the desired shape.    

