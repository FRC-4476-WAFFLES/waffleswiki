
# What are Trajectories?

Trajectories are paths that a robot follows to autonomously drive to different points around the field in a fast and reliable way.
# Choreo Trajectories

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
>  Yes, you have to spend time learning a new tool, but if it saves a bunch of time not having to test and tweak paths, you’re going to have a net time savings if you need to manage a bunch of autonomous modes.

The downside for Choreo is it's not able to run on the fly generation; meaning for tasks like aligning to a node in the 2023 game, we would have to use PathPlanner for that. 
## Choreo
![](https://www.chiefdelphi.com/uploads/default/original/3X/d/1/d19ece50b5decd0f791ac69af719c643dddc92c5.gif)
## Path Planner
![](https://www.chiefdelphi.com/uploads/default/original/3X/4/9/49554a9d337bdb9561b89b7d65dfe37835efafbb.gif)

# What do we Use?

In 2024 we used PathPlanner only. Even though it generates slightly slower paths which make it harder to execute everything in autonomous, it has features that allow it to recalculate on the fly if the robot gets bumped. These corrections lead to a more reliable autonomous, rather than being lost after a teammate bumps you out of the way.