# Helpful External Addons

## Resource Link
* Find all the required external addons in this [website](https://gfxfather.com/) for free.

## Installing Addons
* Go to **Edit->Preferences**
* Select **Add-ons** from the left side bar.
* Now select **Install** from the upper panel.
* Locate the **zipped** file but make sure it contains only the required code files. Otherwise it won't be installed.
* Select **Install Add-on** and it will be installed.
* Then you can **Refresh** or restart the software and search for the add-on. It will be found.

## MACHIN3tools (Paid)
* Enable **Smart Vert, Smart Face, CleanUp, Focus** from tools. These are really important.
* Enable **Modes Pie, Save Pie, Shading Pie, Views Pie, Alignments Pies, Cursor and Origin Pie** from Pie Menus.
* You can check or change the key bindings from **Keymaps**.
* You need to disable **Toggle Cavity** from Modes Pie because it will switch cavity based on modes and that's irritating.
* The **Tab** menu is overwritten. 
    * When we press in **Object** mode, the pie menu contains: **Edit, Vertex, Edge, Face**. We can directly move to these modes from **Object** mode.
    * Pressing in **Edit or others** mode, it provides **Object mode and others**.
        * Also provides **Occlude mode** which is the X-Ray mode.
        * **Auto Merge** which merges vertices while close to each other. In vanilla blender, it takes quite a few steps to enable this feature.
* **Shift+S** This is the same thing as in the vanilla blender just coming in a pie menu. You can set origin and cursor according to need. 
* Merge vertices in the median: - **Shift+1**.
* Merge vertices at Last: - **1**.
* Hide/Unhide Collection: - **Shift+Collection number in Scene Collection**
* To move vertices to particular side: - **Alt+A** and select where you want to s



## BoxCutter-HardOps
* Install **BoxCutter** at first, then **HardOps**.
* Activate **BoxCutter** tools by pressing **Alt+W**. Again pressing will give the **HardOps** tools. We can also do this by directly clicking on them.
* Go back to normal blender tools by pressing **W**.

## BoxCutter

* Boxcutter is an add-on for booleaning objects together. It's very powerful and much more than this.
* Activating this add-on will provide a simple toolbar at top. If it doesn't appear, then
    * Press **N**
    * Goto BoxCutter->Display
    * Enable Simple Toolbar
    * Disabling it will provide a much more complex toolbar.

#### Basic function
* Select the object.
* Create a cut by dragging the box using mouse and release.
* Then make depth of the cut moving the mouse back and forth.
* Left click then it the cut will be executed.
* If we right click before left clicking, then the cut will be cancelled.
* Now after releasing, if we double left click, then it will cut through the object till end.
* It will create a new collection with boolean cutter and hide the collection of shapes.
* Pressing Shift+Left click will keep the cutter visible and parent the base object to shape.

#### Box Helper Operations
* Pressing **D** pops up the box helper menu.
* The operations work on view we work. It's a better idea to work on an orthographic view.
    * **Cut**: Difference boolean.
    * **Slice**: It creates 2 seperate objects and these can be modified individually. But before that we have to go to modifier and apply the boolean.
    * **Intersect**: Anything that is a shared space is going to be created. 
    * **Inset**: It insets and performs a lot of works in the background to create inset series of faces.
    * **Join**: This joins the object. 
    * **Knife**: This doesn't add any modifier. It performs the task of knife tool. 
    * **Extract**: It takes the collection of booleans and perform cut operation as the combined shape of the booleans.
    * **Make**: It allows us to draw a new object and this will be parented to the selected object. Without selection of the object, the shape created using any of the function will create a seperate object and will be counted as the make function. But they will not be parented. 
* Any of these operation will apply the required **Boolean** modifier and the **Auto Smooth** modifier automatically.

#### Set Origin
* We can also change the origin of the shape from the helper menu before creating the shape.
    * **Mouse Position**: Sets the origin from where we start dragging.
    * **Center**: At the center of the starting face.
    * **Bounding Box Center**: Center of the object.
    * **Active Element**: At the origin of the selected object.
    * It's better to use the default option that is **Bounding Box Center**.

#### Shape Type
* **Box**
    * We can change from **Box** to **Line Box**. In the first click, it will draw 1st dimension, then 2nd and 3rd. We can draw lines with angle. We can change line orientation in different angles and it will move on 15' variance. If we don't want any angle then we can move freely by holding **Ctrl**.
    * The default is activated as Shape Type **Box**. We can change those accordingly.
* **Circle**
    * It will perform other operations as same but in circle shape.
    * We can set the number of verices according to need. 
    * We also have **Line Circle** to create deformed circle.
* **N-gon**
    * We can create a **N-gon** shape according to us for use.
    * Double clicking will activate the shape and then moving mouse back and forth will cut through the object.
    * Switching to **Cyclic** won't connect the joining and opening vertices.
    * In **Cyclic** mode, after releasing if we press **T** then moving the mouse will change the thickness of the lines. 
    * Enabling **Lasso** allows us to perform free hand drawing and create shape.

* Without the exception of the knife tool, everything is done **Non-Destractive**ly. That means we can remove the boolean modifier if not needed and apply it for the parmanent shape. But switching to **Destructive** settings will apply the modifier automatically.

#### Orientation
* **Object**: Whatever shape is drawn, the shape is objected perfectly to the shape. There are some more options available. **Local, Nearest Edge, Longest Edge & Face Fit**. All these options fairly do the same work. The default is **Local** and it can be left like this. 
* **View**: It aligns with the view, we are looking from. It does not orient with the object. It directly cuts through the object.
*  **Cursor**: The shape is aligned with the cursor placement. Therer we can also change the axis.
* **World**: It also performs the same thing as cursor but in a bit different way.

#### Snapping and Grids
* Enabling this will create the object in that place.
* Go to particular place and press **Ctrl**. It will show **Static Dots** and we can draw from there.
* Enabling **Static grids** will show grids. The grid is generated based on the center of the shape. We can also change the size of the grid distance. 

* Find the complete beginner tutorial guide to **BoxCutter** [here](https://youtu.be/3zLBmHVXpsk?si=24hZ6p0fefC5_by9). 


#### HotKeys
* Box Helper Menu: **D**
    * Normal: **D**
    * Box Helper Pie Menu: **Ctrl+D**
    * Place mouse pointer on the selected object and press **D**. It will show same menu but in a different way. We can perform operations from choosing there.
* Lock shape before confirming: **Tab**
* Move shape: **G**
* Rotate: **R**
* Rotate 90: **Ctrl+R** 
* Extrude in locked form: **E**
* Bevel: **B**
* Bevel width: **Move mouse back & forth**
* Segment number for bevel: **Sroll Mouse Wheel**
* Bevel in the backwall of the shape: **Q**
* Bevel in the Frontwall of the shape: **Shift+F** after pressing **Q**.
* It's a better idea to perform operations in lock mode.  
* Make Cutter visible: **L** before executing the cutter. It's a persistant feature. If we don't want it we again have to press L.
* Add array modifier: **V**
    * Side change: **Move Mouse pointer to the chosen side**
    * Distance: **Move Pointer back and forth**
    * Axis change: **X** 
    * Radial design: **V** again
* Thicken Modifier: **T**. It turns the edge of the box into a thicken feature. We can adjust which shape we want to thicken. In the case of **Inset**, it thickens the insetted shape.
    * Equally: **2**
    * Inside shape: **3**
    * Outside shape: **1**, default.
* Enable magic dots on face: Press **Ctrl**. Make sure the **static dots** is enabled from the top.
* Backface scaling/ Tapper: **Shift+T**
* Wedge Cut: **W**, press again to change the side. It appears on the faces from the corner we start dragging the shape using mouse.   
* Helper dots appearance: **Alt+D**. We can perform any kind of operation on individual edges by selecting and move, rotate or others.
    * Select any dot and press **Middle Mouse Button** to bevel.
    * **Scroll wheel** for controlling the segment number. 
* Find all the hotkeys and navigation things to **BoxCutter** [here](https://youtu.be/dC2Zw8GcxxU?si=U7lE-NgV1bou9Jwe). 
* Refer [here](https://boxcutter-manual.readthedocs.io/en/master/hotkeys/) for more hotkeys.




## HardOps

* **Inset/Outset: -**
    * Create the changing shape.
    * Select the shape at first and the object secondly simultaneously.
    * Press **Q** and go to **Booleans->Inset/Outset**.
    * The cutter shape will automatically be added to the **Cutter** collection.

* 
* Resharp Shading: - Select object, press **Q**, then press **Ctrl+Shift** and click on **Sharpen**.
           
