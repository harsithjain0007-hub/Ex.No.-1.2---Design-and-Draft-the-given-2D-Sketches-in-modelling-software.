# Ex.No.-1.2-Design and Draft the given 2D Sketches in modelling software.
## DATE:20/11/2026
## REF NO: 26014758

## AIM
 To sketch the given drawing with dimensions using fusion 360 tool.
 
## REQUIREMENTS
 1. Autodesk fusion 360
 2. Windows 10
 3. 16 GB of RAM (integrated graphics recommend 1 GB or more)
 4. 2.5 Mbps or faster download; 500 Kbps or faster upload 
 
 ## PROCEDURE
 ### Step 1: Document Setup and Workspace Selection

1. Open **Autodesk Fusion 360**.
2. Click on **New Design** and ensure the active unit system is set to **Millimeters (mm)** (check under *Document Settings* in the browser tree).
3. Select **Create Sketch** from the **SOLID** toolbar and choose the **XY Plane** (Front Plane) as the sketching surface.

<img width="681" height="788" alt="image" src="https://github.com/user-attachments/assets/ba493ed0-26e0-473a-b49c-4f4dd0691836" />


### Step 2: Drawing Centerlines & Establishing Origin

1. Press **L** for the **Line** tool, press **X** to toggle **Construction Mode**.
2. Draw a vertical axis line passing through the Origin (0,0) and extend it vertically.
3. Draw a horizontal axis line passing through the Origin (0,0) to serve as the main horizontal center axis.
4. Set precise center points relative to the origin (0,0):
   - **Central Hub:** Located directly at the origin (0,0).
   - **Top-Right / Bottom-Right Hole Centers:** Set at horizontal offset X = 50 mm and vertical offsets Y = +60 mm and Y = −60 mm.
   - **Top-Left / Bottom-Left Hole Centers:** Set at horizontal offset X = −50 mm and vertical offsets Y = +60 mm and Y = −60 mm.
   - **Middle Side Hole Centers (Left & Right):** Positioned along the horizontal center axis (Y = 0):
     - Right Middle Center: X = 50 + 20 = 70 mm.
     - Left Middle Center: X = −(50 + 20) = −70 mm.

<img width="755" height="650" alt="image" src="https://github.com/user-attachments/assets/44ffb409-4f52-4272-a187-c7bc98e541dc" />
   
### Step 3: Constructing the Central Hub Features

1. Press **C** (Circle Tool) and disable construction mode (**X**).
2. At the Origin (0,0):
   - Draw the central inner circle with **Radius R15** (Diameter = 30 mm).
   - Draw the middle concentric circle with **Radius R21** (Diameter = 42 mm).
   - Draw another concentric circle with **Radius R32** (Diameter = 64 mm).
   - Draw the outer concentric circle with **Radius R40** (Diameter = 80 mm).
3. **Web / Spokes and Slots Construction:**
   - Create two vertical construction lines spaced 6 mm apart (3 mm on each side of the central vertical centerline) to define the vertical slot boundary.
   - Draw radial lines at 60° increments between the **R21** and **R32** circle bounds to form the 6 segment slots.
   - Alternatively, create one radial spoke feature and use **Create > Circular Pattern** around the center point (0,0) with Quantity = 6.
<img width="267" height="71" alt="image" src="https://github.com/user-attachments/assets/634c28b7-61f7-402f-89d6-42e73f31e740" />
<img width="320" height="257" alt="image" src="https://github.com/user-attachments/assets/6e67fd8b-1872-459c-bba8-ea46f83cbccd" />
<img width="702" height="572" alt="image" src="https://github.com/user-attachments/assets/94fd81ae-c382-4995-b451-77a159a052d5" />

### Step 4: Drawing Outer Circular Bosses and Holes

1. **Top-Left & Bottom-Left Bosses:**
   - At center (−50, 60): Draw inner circle with **R15** and outer arc/circle with **R21**.
   - At center (−50, −60): Draw inner circle with **R15** and outer arc/circle with **R21**.
2. **Middle Left & Right Bosses:**
   - At center (70, 0): Draw inner circle with **R15** and outer arc/circle with **R20**.
   - At center (−70, 0): Draw inner circle with **R15** and outer arc/circle with **R20**.
<img width="606" height="707" alt="image" src="https://github.com/user-attachments/assets/2e7a3ede-cf1d-459c-b96e-6eb2c2502389" />


### Step 5: Connecting Profiles with Tangent Arcs & Fillets

1. **Outer Side Slanted Boundary:**
   - Draw tangent lines connecting the outer arc of the top boss (**R21**) to the middle side boss (**R20**) on left side.
   - Apply the **Tangent Constraint** between each straight line and the corresponding arcs.
2. **Inner Concave Transition Arcs:**
   - Between top bosses (**R21**) and central outer boundary (**R40**): Create fillet arcs of **Radius R16** and **Radius R20** using **Fillet** or **3-Point Arc** with **Tangent Constraint** applied to both connecting curves.
   - Between bottom bosses (**R21**) and central outer boundary (**R40**): Create fillet arcs of **Radius R20** tangentially connecting the geometry.
   - Between middle side bosses (**R20**) and top/bottom outer arcs: Apply tangent connection arcs of **R20** as indicated.
<img width="245" height="376" alt="image" src="https://github.com/user-attachments/assets/e8ffa29d-9178-4ee5-8c83-54bdaa9ec3ba" />

<img width="522" height="567" alt="image" src="https://github.com/user-attachments/assets/a424332d-5a55-47a1-9cad-67b9bc0df439" />


### Step 6: Trimming and Final Constraint Checking

1. Press **T** (**Trim Tool**) to remove unwanted construction arcs/segments inside the outer boundary.
2. Check that all sketch entities turn **black** (indicating the sketch is **Fully Constrained**).
3. Verify all dimensions:
   - Center distances: 50 mm, 60 mm, 20 mm, and vertical slot width 6 mm.
   - Radii: **R15, R16, R20, R21, R32, R40**.
<img width="235" height="280" alt="image" src="https://github.com/user-attachments/assets/f56e0a5f-1a5a-4517-9aed-1cc565a6dd4a" />
<img width="636" height="598" alt="image" src="https://github.com/user-attachments/assets/64f6958b-63cf-4bd3-aa04-9a214845f1bf" />



### Step 7: Mirroring the top-left side to down-left side

1. **Select Tool and Objects:** Go to **Create > Mirror** in the Sketch menu, ensure **Objects** is active, and select the top feature geometry (R21 outer, R20 middle and R30 inner circles, along with the connecting tangent lines located 60.00 mm vertically above the center line).
2. **Set Axis and Apply:** Click **Mirror Line** in the dialog box, select the horizontal center line (passing through the R20/R30 lower-left circles and R40/R32 right slot feature), and click **OK** to generate the symmetrical lower geometry.

<img width="267" height="71" alt="image" src="https://github.com/user-attachments/assets/7865c284-8aaf-445d-99c1-94a4fd242199" />
<img width="805" height="737" alt="image" src="https://github.com/user-attachments/assets/5f7b9865-c66e-4cdd-932e-c4e046b71c49" />


### Step 8: Mirroring the left side to the right side

1. **Select Tool and Objects:** Go to **Create > Mirror** in the Sketch menu, ensure **Objects** is active, and select the entire left-side geometry (R20 / R15 middle-left circles, top/bottom outer profile contours, top circles with R21, R20, R15 and bottom circles located 50.00 mm and 20.00 mm horizontally from the center axis).
2. **Set Axis and Apply:** Click **Mirror Line** in the dialog box, select the vertical green Y-axis center line (passing through the center of the R40, R32, R21, and R16 slot feature), and click **OK** to generate the symmetrical right-side geometry.

<img width="1021" height="745" alt="image" src="https://github.com/user-attachments/assets/d83e6304-b137-4fb8-b6bb-6af314a8cfb4" />


### Step 9: Check the complete outline

1. Make sure all the required circles, arcs, holes and internal cut-outs are present and properly connected.
2. After checking the sketch, click **Finish Sketch**.
3. The completed 2D sketch is then ready for the required drafting.
<img width="220" height="132" alt="image" src="https://github.com/user-attachments/assets/f478d761-0dfc-400f-87df-59ed97903965" />

## SKETCH
 ![image](https://user-images.githubusercontent.com/113594316/198233336-dd9f5c19-481b-486a-928a-99c32a732f89.png)

 ## OUTPUT
 <img width="2191" height="1548" alt="EXP 1 2" src="https://github.com/user-attachments/assets/b6753b3a-45fe-45b7-8146-9de349001daf" />

 
 ## RESULT
 Thus the given sketch is drawn and drafted using fusion 360 tool.
