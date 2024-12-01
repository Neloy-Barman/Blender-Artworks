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

## Inverse Kinemetics
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
