---
tags:
  - blog
date: 2023-12-10
---
# Topics
- Choreo Trajectories
- Part Templates, Configurable Parts and BOMs
# Choreo Trajectories

This all relates to [[Robot Trajectories]]

[Choreo](https://www.chiefdelphi.com/t/introducing-choreo-a-new-approach-to-swerve-trajectories/445236) is a new trajectory library that specifically optimizes for path speed. In 2023 we used [PathPlanner](https://www.chiefdelphi.com/t/pathplanner-2024-beta/442364). A big advantage is that you don't have to tweak paths to make them faster. Current tweaking using PathPlanner you often make requests of the robot to follow a path that it physically cannot actually do. Choreo helps a lot in this case with getting fast paths up quickly.

> [!quote] mjansen4857 3015 Programming Mentor
> The whole point of Choreo is to not have to spend a lot of time tweaking paths to get it to do what you want. For example:
> 1. Run the path, it overshoots a curve
> 2. Change the path to slow down at the curve or increase the curve radius
> 3. Run the path again, its translating too fast while rotating, causing error to build up from module saturation
>4. Slow down translation along the rotation
>5. Run it again, auto takes longer than 15s now
>6. Try to speed up some sections and shorten others
>7. It overshoots a curve again
>8. Repeat
>   
>  PathPlanner gives you a lot more control over your path compared to Choreo, but as a result, you can make a path the robot just can’t physically follow. When you do this, you’re going to have to do a lot of testing and tweaking to get it to a point where the robot can follow it. I literally made PathPlanner, but it still takes our team hours to tweak and test paths to get them to a good spot. That’s just how it works. Choreo tries to remove a lot of that testing and tweaking time by calculating a path that the robot can actually follow accurately from the beginning.
>  
>  Yes, you have to spend time learning a new tool, but if it saves a bunch of time not having to test and tweak paths, you’re going to have a net time savings if you need to manage a bunch of [[autonomous]] modes.

The downside for Choreo is it's not able to run on the fly generation; meaning for tasks like aligning to a node in the 2023 game, we would have to use PathPlanner for that. 

Currently the PathPlanner team is working on integrating Choreo support in their ui.
## Choreo
![](https://www.chiefdelphi.com/uploads/default/original/3X/d/1/d19ece50b5decd0f791ac69af719c643dddc92c5.gif)
## Path Planner
![](https://www.chiefdelphi.com/uploads/default/original/3X/4/9/49554a9d337bdb9561b89b7d65dfe37835efafbb.gif)

\- Brennan
# Part Templates, Configurable Parts and BOMs

My GitHub Desktop was broken for a few weeks but we're back with a ton of very new and very cool (I think) CAD stuff!!
## Part Templates

To create some parts quickly and without human error, I have created some part templates for 0.5" churro, round tube and rounded hex. If you want to take advantage of these, you'll need to add the "4476 SolidWorks Templates" folder to the list of "Document Template" file locations (learn how to [[Add File Locations]])

Once the file location has been added, you'll be able to create any of these parts directly from the New Document window. All you'll have to do is choose the type of part you want to create, then change a few parameters on your own. As of now, we have part templates for the following components with their respective adjustable parameters:

- 1/2" Churro, change length
- Round Tube, change outer diameter (1/2" or 3/8") and length
- Rounded Hex, change hex size (1/2" or 3/8") and length
- 3D Printable HTD 5mm Pulley, change tooth count and width (very broken, will fix later)

![](https://i.imgur.com/0UNqEOc.png)

The beauty of these part templates is:
a) Makes it very easy and quick to make common parts with no errors, and
b) They have fancy properties built in that automatically update in the assembly bill of materials
(more on that later in this blog)
## Configurable Components

Update to the [[29th October 2023 (Sunday)|October 29th Blog]]: new configurable components have been added to the [[4476 Parts Library]]!
- Bearings (various inner diameters, outer diameters, hex bores, flanges)
- Flanged Bushings (various inner diameters, outer diameters, flanges)
- Socket Head Cap Screws (#10-32 and 1/4"-20, various lengths)
- Button Head Cap Screws (#10-32 and 1/4"-20, various lengths)
- Nylock Nuts (#10-32 and 1/4"-20, standard and slim sizes)

Again, to choose which version of each component you'd like to use, you can right click the part and change the active configuration in your assembly.

![](https://i.imgur.com/sDiOr1B.png)
## Bill of Materials

A Bill of Materials (BOM for short) is a list of components that are in an assembly. It usually only lists the part name and quantity, but we've gotten it to display a few more additional pieces of information:

![](https://i.imgur.com/Hd4qHzC.png)

As long as you use the 4476 BOM Template when you create the table (it's in the 4476 SolidWorks Templates folder in the [[4476 Parts Library]]), the Description and Length columns will appear to show the configuration of the part as well as the length of shafts. There will probably be a column added to show the material of the part as well, that will be done at a later date.

The best part is that we can save the BOM as an Excel table, then copy everything into a Google Sheet. This lets us make an efficient parts tracker during the build season (we'll probably write a blog on that soon - watch this space)

\- Brandon
