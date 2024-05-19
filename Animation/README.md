# Animation Tools

## Hotkeys
* **Spacebar** is used to play the scene in blender. 
* **Alt + Scroll Wheel** to move the keyframe.
* Inserting keyframes - **I**.
* Duplicating keyframes - **Shift + D**.
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
