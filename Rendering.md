# Rendering


## Must enabled properties
* Go to **Render Properties**
* Turn on **Ambient Occlusion**.
* Turn on **Bloom**.
* Turn on **Screen Space Reflections**.
    * Enable **Refraction** for the transmissive objects. 
* Go to **Shadows**. Enable **Height Bit Depth** and **Soft Shadows**.
These settings will make the scene with lighting look more attractive and eye-catching.


## Viewing Render result
* Go to **Rendering** tab.
* Keep **Render Result**.
* Go to **Render** tab.
* Click on **Render Image or Animation** whichever you want.


## Exposure
Sometimes there is a problem with the render and that's a little bit of exposure of the scene.
* Go to **Color Management** tab, play with the **Exposure** value.
* Set **Look** to comfortable style. 


## Render Engines
### Eevee 
We can get a really nice render with **Eevee** render settings whether it's an animation or more cartoonish  look rather than realistic looks. It works like a game engine. So, to work properly, to bake lights properly, we need some probes.
* Adding **Light** probe: **Shift+A-> Light Probe -> Reflection Cubemap**. Scale this to large to make this around scene.
* Then add **Irradiance Volume** in the same way. It is used to bake the illumination. Also make this larger to fit the scene.
* Now in **Render Properties -> Indirect Lightings**, you can **Bake Indirect Lighting**. It's basically taking into account all the emission lights. It means all the lightings we can see in the materials. But it takes into account the **World light** as well. So, before baking the light, change the **World Settings** according to need.
* When you **Bake Indirect Lighting**, you can see the scene coming into life. Materials take light information from the sources and bake it more and more.  
* When rendering even **Hidden** objects are rendered. So, make sure the **Disable in Render** is enabled for the objects from the parent to child.
* The rendering in **Eevee** is fast and the result is great.
* To save the image go to **Image->Save as**. The rest is known.


## Cycles
* When working with this render engine, viewing the object in the **Rendered** viewport is costly. To solve this issue, view in **Material Preview**, go to top right panel and click on **Viewport Shading**. Enable **Scene Lights** and **Scene World**. You will get a similar preview to the **Rendered**. So, look and adjust settings in **Material preview** and then go to **Rendered**.
* Go to **Render Properties**, set the **Render Engine** to **Cycles**. Device to **GPU Compute** if GPU available.
* Go to **Sampling**,
* Enable **Denoising**.
* In **Render**, set **Max Samples** to 512 or higher to ensure a high quality image rendering.
* **Light Paths** settings determines how many bounces the light does for each channel in the scene.
    * Sometimes we have a problem called **Firefly**. It's basically when we have a lot of lights in the scene and while rendering, there are a lots of dots in the image. These are over exposed pixels. At that time, we have to clamp the lights to avoid them.
        * In **Clamping**, change the **Direct Light** and **Indirect Light** values to fix these according to need. 
* Rendering in **Cycles** take a lot of time. But it also gives a good result. 


### Bloom in Cycles
Bloom is a post-production effect where it just takes the lighting information of the rendered image and applies some effect to it. There is a way of doing bloom in cycles.
* Go to **Compositing** tab from the top panel. This is for applying some transformation, color correction, effects to the rendered layer. Enable **Use Nodes** to see the available layers.
* Before applying some effects, you need to see the **output** of what you are doing. So **Shift+A**, add **Output->Viewer** and connect to the **Image**. The output will be shown in the background.
* Go to **Side Panel->View->Fit** for the image fitting in the background.
* Add **Filter->Glare** filter. Connect nodes properly to see the output. This adds some scientific glares to the image.
    * Change the effect to **Fog Glow**. 
    * Tweak the **Threshold** to get proper effect. Lower the value more the effect and vice-versa.
* Now go to **Rendering**. Swich from **Render Result** to **Viewer Node**. Save the image then. 
