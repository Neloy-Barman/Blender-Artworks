# Coloring Objects

* To give color to an object, select the **object**, go to **Material Properties**, create new **Material** and assign the chosen color to the object.
* If you have multiple objects, and you want to assign the same color from a partiular object, then Select the colorless objects and the colored object in last, then press **Ctrl+L** and select **Link Materials** to color the other objects.
* To create a same color in different shades, you can duplicate color from **Add New Material** and change other properties based on preferences.
* If you want a color to emit, then change the **Surface** to **Emission** shader and change the shader strength according to need.    


## Water Object
* Choose **Base Color**.
* Change **IOR, Transmission** values.
* Set **Roughness** to the least value to get better results.


## Metalic Object
* In the **Material Properties**, change the **Material** to **1.00** behave the object like a metal.
* Decrease **Roughness** to make the object look **smoother**. The less the **Roughness** value, the more the shiny the object is.


## Glassy Material
* Set **Roughness** to **0**.
* Set **Transmission** to close to **1**.
* If we like the material to be transmissive, then we need to edit some settings in **Evee**.
* We have to enable **Screen Space Refraction** in settings.
* It determines how deep the material will simulate the rays going into the object.


## Random Coloring for duplicated objects
* Add **Material** to the object in **Shading's Node** panel.
* Add **Converter->ColorRamp** and set desired number of base colors for the objects. Also change it to **Constant** from **Linear**.
* Then insert an **Input->Object Info**.
* Connect **Object Info Random** node to the **ColorRamp Fact** node. Each object will generate random numbers and a new color will be assigned based on that. 
* Now connect the **ColorRamp Color** node to the **Materials Base Color** node. 