(insert video embed)

For those who have used SolidWorks before, you'll have created parts individually, then used mates to create an assembly of parts. This is called the **bottom-up approach** where the dimensions of the parts are defined individually, so changing the geometry of parts once the assembly has been built can be a challenging and time consuming process. 

Alternatively, SolidWorks also supports use of a **top-down approach** where parts are defined in relation to each other. The workflow goes roughly as follows:

1. Create a part file containing only a layout sketch
2. When creating parts of an assembly, insert the layout sketch part before creating any geometry so that you can base your parts off the sketch
3. Insert custom parts into an assembly (very few mates are required)
4. Insert COTS parts into the assembly
5. Edit the layout sketch whenever geometry needs to be changed, and watch the parts and assembly update accordingly

Now, a deeper dive into each step:
## Layout Sketch

![](https://i.imgur.com/oPn2UIQ.png)

The first step of the process is to create a part file that contains only the layout sketch. This layout sketch dictates all crucial geometry of a subsystem and should roughly include the following:

1. Define requirements of the system
	- Chassis
	- Extension limits
	- Pickup and scoring locations
	- Climbing bar height
2. Define desired geometry
	- Location of rollers on an intake
	- Shooter wheel location, hood compression on a shooter
	- Arm length and pivot locations on an arm
3. Define connecting geometry
	- Connecting bars on an intake
	- Structural extrusion/plates on a conveyor
4. Define powering mechanisms
	- Gearboxes
	- Belt an chain systems (check [[Center to Center Distance]])

It's recommended to split each of these layout stages up into separate sketches to keep dimensions and relations readable and usable.
### The 3rd Dimension

If you've followed the steps above, what you'll have is a detailed **base sketch** with a lot of the details on how your assembly actually works in 2 dimensions. However, you'll still need to define everything in the 3rd dimension to fully dictate what your assembly will look like.

Start a sketch on a perpendicular plane (e.g. if you created your first sketch on the right plane, make a sketch on the top or front plane) and sketch out the thicknesses and locations of your plates, gears, motors etc. This will be your **3rd dimension sketch**.

A 3rd dimension sketch is needed for all 4 layout stages, each should include:
- Positions of components in the last direction (whichever has not yet been dictated by the base sketch)
- Plate thicknesses (size of the plate does not need to be defined)
- Hex shaft lengths
- Space to account for bearing flanges

Be sure to reference your first sketch wherever possible! Take this intake pivot gearbox for example: The **size** and **longitudinal** + **vertical locations** of the motor, gears and sprockets are defined by a **base sketch** on the right plane, and the **horizontal positions** of all these components are defined by a **3rd dimension sketch** on the top plane. Points are added to the base sketch so that the longitudinal position of each component can be referenced by the top sketch using coincident mates.

![](https://i.imgur.com/uIBA1XV.png)
![](https://i.imgur.com/ovDz8zk.png)