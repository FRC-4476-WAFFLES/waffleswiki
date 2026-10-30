Follow normal naming guidelines - Side(If applicable) - tool

EX: 310-P-003-Top-4mm

EX: 420-P-010-Left-6mm

If a layout with multiple parts is being made then it shall be named

Material - DDMMYY - Part Count - Tool

EX: 4 parts from aluminum on Sept 30th, 2024
- 6065Aluminum-300924-4-4mm


Once in Solidworks with the part open
1. Navigate to CAM Tab
2. Right click on operations to create a new job (template selection)
	1. 1. Model -> Select all Models being cut
	2. Stock Size -> Relative Sized Box, Add Stock to Sides and Top-Bottom-> Stock Side Offset 1in
	3. Work Coordinate System -> Use X-Axis and Y-Axis
		1. Pick an edge for each that will be in the X and Y axis of the CNC, usually the closest and farthest left
	4. Reverse if needed to get the origin arrows pointing in the right direction
		1. X = Red
		2. Y = Green
		3. Z = Blue
	5. Origin -> Stock Box Point -> Top Corner 1 (usually, but change to whatever gets to the most Negative X and Y point)
	6. Machine -> WAFFLES-CNC
	7. Post Processing -> DO NOT TOUCH, ensure offsets remain ZERO
	8. Confirm with green checkmark at the top
3. Press add from template (above)
	1. Name the Job according to the operation -  Bore/Pocketing
	2. Right click on the Template -> Edit
	3. Navigate to second Tab (Blue Pyramid)
	4. Select entities to be cut
		1. Bore's are only holes and need to select inner wall of cylinder
		2. Pocketing can be anything, select the top edge of a cut out and ensure the arrow is on the WASTE side of the cut. Use reverse button if needed. 
	5. Accept with green checkmark
4. Sanity check, the 3rd tab under the job should now indicate some size (500bytes or more)
5. If multiple operations with the SAME TOOL must be made on the same side of a part, add an additional operation
6. Otherwise repeat this process for a new side and/or tool and/or part
7. Finally, once the entire job is complete, press Generate Toolpath by right clicking the job
8. Use the Simulate feature to ensure the job will execute properly
9. Once the simulation has been shown to a mentor, press post process
	1. Change output folder to whichever is appropriate for the part
	2. Name the .nc file based on convention (see top of this docs page)
	3. Change unit to MILLIMETERS (VERY VERY IMPORTANT)
	4. Press Post then save in the file explorer
10.  G -code is now ready
	