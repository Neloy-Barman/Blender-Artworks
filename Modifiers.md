# Modifiers


### Array
**We can create same object multiple times. Set fixed count number and tweak the values of dimensions according to need. Such as, Stairs steps.**


### Boolean
**We can intersect, combine and subtract portions among objects.**


### Curve
**Selecting an object, we can merge it into the bazier curve. Then the geometry will be presented according to the curve properties.**


### Displace
**We manipulate an object with different textures by applying and tweaking the properties values.**


### Skin
**Creating a custom geometry, we can give it a skin or volume. To change the thikness of the skin, you have to turn on vertex selection mode, then pressing Ctrl+A, we can scale the skin. For example we can create railings, custom trees using this modifier.**


### Wireframe
**This modifier is similar to skin modifier. But applyig this one, we can give metalic vibe to the object. Such as, rod stairs, metalic frames.**


### Solidify
**This gives a proper volume to the geometry. For example, giving volume to the buidling, leafs, car body and many more. Enable Even Thikness to get proper solidifying from all sides.**


### Mirror
**This is the perfect modifier to give symmetrical vibe to anything. The cursor should be in the middle of the mirror objects. When you extrude things from one side, the for some cases they overlap. That's why You should use clipping to merge them properly. To make symmetrical objects you can go to Mirror Object and pick the object using dropper tool.**


### Subdivision Surface
**The algorithm sub-divides our geometry non-destructively. Increasing the Render number in the modifier gives us the best results. If we want to control the geometry, then we have to add some more loopcuts to get a better result. It almost works like bazier curves.To get sharper and smoother corner, add loopcuts from all ways.**


### Bevel
* **Does the same thing as the Bevel using Ctrl+B. But it applies beveling on the whole object and all the edges.**
* **To make the shape circular, we need to change the Geometry->Miter Outer to Arc. Then it will give a rounded shape for the required places.** 
* **But it introduces some wierd beveling within large surfaces. To Fix that, we need to add a new modifier that is Weighted Normal.**
* **To solve the proble of shading for a particular edge, we can introduce another bevel modifier in the stack. Change the Limit Method from angle to Weight. Then select the edge and right click and select Edge Bevel Weight. This will solve the issue of shadowing.**

### Weighted Normal
* **This solves the issues of shading problem created by the bevel modifier.**
* **This modifier should always be at the bottom of the stack.**
* **Never apply this modifier to the object even at the final processing.**
* **Just apply it in the end and don't touch it.**

### Edge Split
**Edge split modifier simply splits the edges into multiple meshes. When we do simple smoothing but also don't want the beveling angles to be shown, in that case, we can apply this modifier and the work will be done. There is one value which decides what will happen. That's the Edge Angle. Changing this value can affect the value. It's the angle between phases. If the angle value is greater than 30', then it will split the meshes.** 

**The same thing can be done going to Object Data Properties->Normals-> Enabling Auto Smooth and putting required angle.**


### Screw
**If you want to create an object like drinking glass, wine bottles, flower tob or something like this, then this is the most useful modifier. Just create a shape from one side, then apply the modifier. Boom! The total shape is automatically created. Change the value of Angle, Screw and Iterations to get desired results. Also The number of steps will affect the result. More the steps, more detailed the object is.**

