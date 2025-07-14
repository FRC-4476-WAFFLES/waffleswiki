---
tags:
  - blog
  - CAD
  - design
  - Solidworks
---
# Topics
- 3847 Spectrum Robot Notes
- Top-Down Workflow in SolidWorks

# 3847 Spectrum Robot Notes
## Bearing Plates
![](https://i.imgur.com/kTOauB6.png)While most teams would have a press fit hole for their bearings directly in their plates, 3847 put their bearings in a small plate which is then screwed onto the main plate. They say this makes it easier to do maintenance on the [[intake]] rollers because it is easier to remove all the plates with the bearings in them rather than sliding the hex shaft through the bearing.

This system is great for serviceability and replaceability, but takes more effort to [[design]] as there are now multiple parts and mating clearance holes where there used to be just a single bearing hole. Interesting concept, but I don't think this specific implementation will be used on a 4476 robot.
# Top-Down Workflow in SolidWorks

Designing using a top-down workflow means coming up with the overall geometry of all components first before assembling everything into subsystems, as opposed to the bottom-up approach most students are used to where they create each part individually, then put them together in an assembly.

Over the past year or so I have been getting familiar with the top-down workflow using a "Driving sketch", where I make a SolidWorks part file that only contains sketches that dictate the geometry of the entire robot/entire subsystems. I then insert the driving sketch part into every new component I create so that whenever I change geometry in the driving sketch, the parts will shift to follow. An extra bonus is that there are less mates required in an assembly build from a driving sketch, all parts will be in the right places as long as the origins are all lined up in the assembly.

![](https://i.imgur.com/5MQf7PS.png)
![](https://i.imgur.com/5FabZP2.png)

This top-down workflow makes it very easy to make geometry adjustments once all the parts have been modelled, but involves quite a steep learning curve especially for those new to [[SolidWorks]] and 3D modelling and also requires solid practices to ensure that the model and sketches don't break easily. More detail on this workflow will be published at a later date.

| Pros | Cons |
|---|---|
| Easy to adjust | Steep learning curve |
| Forces students to create layout sketches | Takes time to set up |
| Less mates in assemblies | Need to be careful when multiple people work on a subsystem simultaneously |
| Robust assemblies | 3D geometry is hard to visualize in sketches |

There is another way of doing top-down design in SolidWorks where instead of creating a driving *sketch* and inserting it into every new part, you instead create a driving *part* which includes all key components as separate bodies. Each body can then be saved as a new part, which can then be inserted into assemblies. This may be a more initially confusing approach to some students as the driving part, "formed" part and assemblies can look similar, but once students get the hang of that they'll probably find the 3D geometry easier to visualize than when they use the driving sketch method.

\- Brandon