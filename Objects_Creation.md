# Different types of objects/ shapes Creation


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
 


