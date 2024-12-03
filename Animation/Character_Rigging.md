# Character Rigging
* Make sure the **Rigify** add-on is enabled.
* **Addition of the armature: -** Press **Shift+A**. Now Click on **Armature -> Single Bone**. This will add an armature.  
* **Front view bone: -** To view the bone always in front of the mesh, go to **Object Data Properties** from **Properties** panel. Go to **Viewport Display** and enable **In Front**.
* **Modes: -** The bone has 3 modes, **Object, Edit & Pose mode**. We can animate bone in the pose mode.
* **Display Mode: -** Go to **Viewport Display**, Change the dropdown from **Display As**.
    * **B-Bone:** We can change the size of the bone according to need in this type. **Ctrl+Shift+Alt+S** will change the size of the bone but will not affect where the bone is placed. It will be easier to select important or other bones based on the size.
* **Extrude Bone: -** In **Edit mode**, take a **head** and press **E** to create an extruded part.
* **Rename Bone: -** Click on **Bone Properties** from **Properties**. There we can change the name of the bone.
* **Naming Convention: -** Add a space and then write **L** or **R**. Blender will then use this duplicate the bones on other side.


# Inverse Kinemetics
If we don't have this setup, we have to select each bone one by one for particular things such as for arm or legs and move them one by one while animation. With the **Inverse Kinemetics** rigging, we can select one 
bone and connected parts will be moving automatically. 
* Select the bone inside the IK bone.
* Go to **Pose mode**.
* From **Properties** panel, go to **Bone Constraints**.
* Click on **Add Bone Constraint** and select **Inverse Kinematics** from **Tracking**.
* Now within here for **Target** we need to select the setup **Armature** of the entire object as we are riging using the armature.
* Now for the **Bone**, we need to select the bone which will control this bone. Grabbing the bone we can move the entire armature object. 
* Doing this will move the controlled bone out of the position because it's using the tail.
* Now to reset the position disable **Use Tail**.    
* But we want specific targetted bones to be moved. To do this, we need to change the **Chain Length**.
* When the **Chain Length** is 0, it will move the entire bones within the body. If we change the chain length to 1, it will move the after and before 1 bone connected to it.
* Now we need to occupy an arm to control rotation of the target bones.
* Within the **Pole Target**, select the required **Armature** object.
* Within the **Bone**, select the **Bone** that you want as the rotation controller. 
* Now this will bring all the target bones into the same rotation as the controller.
* Mannually change the **Pole Angle** to negative direction match to the previous angle.
* Now we can copy this rotation to other bone. Select **Copy Rotation** from **Transform**.
    * Within **Target**, select the **Armature** object.
    * Within **Bone**, select the bone whose setting you want to copy.
* If any bone doesn't work expectedly, then just delete the bone, subdivide the working bone and place the parts accordingly to work.
* **Parenting Bone** 
    * Selecting bones, go to **Edit mode**.
    * Select the bone that you want as parent in the end, press **Ctrl+P** and select **Keep Offset**.
    * The bone will be parented to other bone with their respective position.
* **Making bones to not control mesh**
    * Select the bone.
    * Go to **Bone** from **Properties**.
    * Disable **Deform**.
    * Now the bone will not control the mesh.
    * We do this mostly for the **IK** bones because they are just to control other bones combined not for controling the body structure.
* **Mirroring Bones**
    * Select one sided bones in **Edit Mode**.
    * Now go to **Armature** from above panel and click on **Symmetrize**.
    * In the popup panel, you can change **Direction**. It is same as the **Object** Symmetrization thing.
    * You will notice all the bones will have name of their directed side. **L** or **R**.
* Here comes the truth of the moment.
* In the **Object Mode**, pressing **Shift**, Select the **Object** to be rigged and the **Armature**. 
* Press **Ctrl+P** and select **With Automatic Weights**. It will detect where the meshes are with the bones and it rig the bones nearby. 
* If we have individual bones and meshes, select **Bone** to parent. 
* **Editing Weight Painting of Bones**
    * In **Object mode**, select the bones and the mesh in the end.
    * Now go to **Weight Paint** mode. 
    * Select the bone using **Ctrl+Shift+LMB**.
    * It shows the weight paint of the bone. This is a visual representation of how much mesh will the bone pull along.
    * Where the mesh is red, it will pull all the mesh of that area. Closer to blue one means it will pull less mesh from that area. Now going from red to blue and the in between colors means pulling mesh lesser.
    * We can change **Weight, Radius & Strength** values for the brush and paint areas to control the regions with bones.
    * Make sure to set the axis to symmetrize the workings on both side.
    * Now select which brush you want to use from  **Browse Bush to be Linked**. Mostly we will use **Add, Subtract** to control areas.
    * If we select the bones with **Deform** turned off, then the areas will be turned to pink.
Congratulations!!! Now we know the things to create the basics of the character rigging.     