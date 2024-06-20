# Different types of objects/ shapes Creation


## Stairs
### Normal Stairs
* Create the upper and lower step from a plane or anything like edge or vertices. 
* Then apply **Array Modifier** and adjust Factor X, Y, Z value according to need.
* Go to **Edit->Edges** mode and selecting all **Edges**, press **M** and merge **vertices**.
### Metalic Stairs
* Do the same things as the **Normal Stairs** procedures.
* Just apply **Loopcuts** or **Sub-divide** to the whole object.
* Then add **Wireframe** modifier to the whole object.S


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

## Neon Lights
* Duplicate the **Edges** of the **Area** from the object and seperate them as a single object.
* Selecting vertices, apply **Skin** modifier and change the size according to need pressing **Ctrl+A**.

## Texts
* **Shift+A->Text**.
* Selecting the text in **Object** mode, go to **Object Data Properties** to tweak with the properties.
* In **Edit** mode, you can change the text of the object.
* To center the text, in the object data properties, go to **Paragraph->Alignments** and make **Horizontal**, **Vertical** **Center**.
* To change the font style, from **Font**, select regular weight and select particular **.ttf** file. You can use your chosen ones by downloading them from **google fonts** and placing the **ttf** file there.
* To make the text **extruded**, go to **Geometry->Extrude** and change the value according to need. For **Bevel**, the settings is also in the **Geometry**. 
 

 


