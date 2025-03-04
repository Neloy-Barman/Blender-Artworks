# Fundamentals of Realistic Modeling

## References
* Find the **Front, Top, Back, Side** views of the object and the object in **Textured**. It's essential to find proper references of the object you will be modeling. Otherwise when you start and go on, you won't be able to proceed and get frustated leaving the project completion.
* Go for the **Branded Object**. In most of the cases, there will be proper blueprints searching for the object with name.
* Place the blueprints properly on the blender.

## 3 common ways to fix something
* Re-calculate normals
* Merge vertices **By Distance** using **M**.
* Check there are no extra inside **Edges** or **Faces** creating problems.

## Random things to consider 
* In the real worlds, surfaces don't actually intersect. There is a very shuttle gap in between them.
* The gap might not be visible to the eye, but that might add shadows creating more realism to the scene. That's why we need to keep sharp edges. In those cases, selecting the edges, we can perform **Edge Creasing**. 

## Using View
* Make sure to use **MetCap** view and use different ones untill it shows you the better form than the default form. It shows you the reflections and other things.

* When you want to fit mesh in all the orthographic views, make sure to split the windows in those views. This helps to position the vertices in all the views and reduce mistakes.
* Sometimes the edges in a mesh should look straight but these are not and they look winky. In that cases, select the edge. Then press **G+G** for edge sliding. Then press **E** for **Even** mode. This will make the edge straight. If we press **F**, then it will show which side is it defaulting to.
* If we get one vertices way out of the line, then we can do shrink flatten, that is **Selecting Vertex+Alt+S**. It will move the vertex along its normal. You can bring vertices to particular line according to need.    
* Sometimes you need to move vertices using sliding. In that cases, you can disable clamping and move it more further on its axis. **G+G+C**.   
* Don't forget to switch to local axes of the vertices while moving vertices. This will help to keep the shape in its best.

## Overall Scaling
* When we model something from blueprints, we just work on withut any consideration of scaling. But everything in the world has a real world scaling. It's not a problem of having a large scale in the vaccum but it will be annoying when you add something to a scene with incredebly wrong scale. That's why scaling properly is required. It's so much easy when you scale everything correctly. When you import and reuse assets then the things look perfect and correct. We need to make a habit of doing that.
* To do this, at first take a cube, set the **Origin Point** to the base of the object. Then scale the height of the **Cube** to required things.
* Now take the **Object** and perform scaling to make the size perfect.
* Don't forget to perform universal scaling by pressing **Ctrl+A**. 


# Sharper objects
* To make some corners sharper, we can select edges, press **Alt+S** to scale the edges and move accordingly to look it as a sharp edge.
 

