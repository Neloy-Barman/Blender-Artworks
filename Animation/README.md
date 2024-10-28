# Animation Tools

## Hotkeys
* **Spacebar** is used to play the scene in blender. 
* **Alt + Scroll Wheel** to move the keyframe.
* Inserting keyframes - **Select Object+I**.
* Duplicating keyframes - **Shift+D**.
* Change Handle type - **V**.
* Increasing distance between keyframes - **Select all keyframes + S + value**. 


## Introduction
* **Timeline**: It gives us the ability to view and understand timing for our animation. It also controls certain playback options such as frame range.
* **Keyframes**: These are used to tell the computer what poses of the characters we want at different times.
* **Pose Mode**: Pose mode is used to pose the rig. It allows you to dynamically change the pose of the character over time.
* **Dope Sheet & Graph Editors**: These are tools that help us to visualize and edit our keyframes to fine-tune our animation.
* **Curves**: These are more advanced form of keyframes that allows us to fine-tune the interpolation between keyframes. 
* **Cameras**: It will be used to film and render the scene just like a real camera. 

## Timeline

**How the software interprets the time in our scene. It is the foundation of how animation works in blender.** 

* Creating a new keyframe on the existing ones overwrites the existing one.
* Change Loop regions to desired range to see the animation properly.   
* By default, blender interpolates the keyframe poses with an ease in and ease out motion.Slowly transitioning the velocity between poses. But blender allows us to fix interpolation like this. To slow the animation, we can increase the distance between keyframes using scaling.
* FPS value in red means the current playback speed is less than the actual one. 
There  will be cases where our scene will be so heavy that our  viewport won’t be able to handle it. After rendering the actual playback speed will be a lot faster. 
* Go to Playback 
    * No Sync - It is good to view each and every frame. But it costs time. 
    * Frame Dropping - It costs a few frames to drop.
    * AV Sync - It stands for audio visual sync. It prioritizes synchronization of the viewport playback with the audio playback.


# Keyframes
* These are used to tell the computer what poses of the characters we want at different times.
* **Insertion:** Select the object
    * Press **I** to insert **location, rotation and scale** keyframe.
    * Press **K** to popup the **Insert Keyframe Menu** and select the type of frame. 
* The following tasks need to be performed by selecting the keyframe.
* **Editing:** Press **G**. Now move the mouse back and forth to move the keyframe.
* **Deletion:** 
    * Press **Del**. 
    * Also pressing **X** and selecting **Delete Keyframes** will delete the frame.
* **Duplication:** Pressing **Shift+D** to replicate the frame. 
* **Overwrite:** Creating a new keyframe on the existing ones overwrites the existing one. Keep the mouse pointer line on the keyframe and press **I** to add a new one.
* **Auto Keying:** The dot in the timeline panel is the button. If we enable this, a keyframe will automaticallyy added when we transform the object. Using this makes the workflow much faster. 
Once you are done with the animation, make sure to turn it down off.


# Frame Rate
* It tells blender how many frames will there be within 1 second. FPS stands for frames per second.
* The default is set to 24 fps. For most of the cases, 24 fps will be just fine. 
* If we want our animation to be more smooth, then we can turn up the fps to 60. Then our animation will be much faster and more smoother. 
* Go to **Properties** panel and select **Output**, now click on the drop down with the **Frame Rate**.


# Animating other values
* We can animate anything within blender.
* Suppose, we want to animate any kind of value, then selecting the value, we have right click and select **Insert Keyframe**. We can also press **I** directly to insert.
* This will add more than one keyframe in the timeline, one is for the object and other ones are for the selected properties.
* We can view this by expanding the **Summary** within the timeline. We can view where we have the keyframes for the different parts of the object.    


# Graph Editor
* If we want to have more control over the animation and keyframe, we can use graph editor.
* We also get a view of the detailed keyframes within the graph editor.  
* We can see the graph of different animations in the editor.
* We can change the size of the graph editor scrolling the **Scroll Wheel**.
* If we want to slow down or speed up the animation by moving the particular curve back and forth. 
## Handles
* These are very helpful. By moving the handle, we can change the shape of the animation. We can animate in between the certain period to make the animation morre robust.
* **Interpolation: -**
    * Keyframe interpolation menu - Put mouse pointer in the **Timeline or Graph Editor**. Then press **T**. This will bring up the interpolation popup menu.
    * Most used ones are - 
        * **Constant:** This will create very sharp curve. There is no smoothing here. It automatically hops to the next keyframes.
        * **Linear:** It's not gonna slowly speed up or down. It just exactly goes from the first keyframe to second keyframe. It looks very robotic.
        * **Bazier:** It's the default one and most used. It slowly starts and then speeds up and reaches next. So, it works perfectly as required.


# Basic Rigging
* Make shapes accordingly.
* Then select the places where you want the object to get rigged or want to place the joints.
* Set the origin of the to be rigging object to the joint place.
* Then parent base object to be rigging objects.
* Create a chain of these meshes and go on to create the animation. 

* Selecting the object and Pressing **N** will pop up the side menu. Go to **Item->Transform**. Now you can lock the transform you want and keep open which you want to animate. 
* Clearing location and setting all axis to zero: - **Alt+G**.
* Clearing rotation and setting all rotation to zero: - **Alt+R**.
* Clearing scale and setting all scale to one: - **Alt+S**.
