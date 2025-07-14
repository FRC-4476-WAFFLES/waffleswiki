---
tags:
  - blog
date: 2024-01-13
---
Day 8

# Autos

![](https://i.imgur.com/qstMF3n.png)
![](https://i.imgur.com/JCYnNKp.png)
We discussed different viable autos and the order of which we want to do them. There may be some variations that pick up certain notes in different orders, but this is the general list

1. Drive Forward
2. Shoot preload + drive
3. 2 piece front speaker
4. 3 piece front speaker
5. 4 piece front speaker
6. side speaker preload
7. side speaker two piece
8. middle preload speaker
9. steal ? number of pieces
10. preload to middle close, to middle line and clean up left right (5 piece)
11. side speaker 3 piece
12. middle 2 piece
13. bump opponent pieces and just mess them up but don't score
## General Auto Assertions

1. Contest middle pieces but not at the cost of scoring preloads and close pieces
2. Contest middle pieces as early as possible to beat defenders/other robots from stealing notes.
3. Make sure to have three viable auto start positions to be flexible with potential partners.
# Intake High Fidelity

We cut and assembled our high fidelity intake that has in theory good geometry for going from under the bumper to over the swerve module.

INSERT VIDEOS

To start we had issues actually picking up the note, our sharp bend radius caused the note to get stuck on supporting churros across the length of the intake

We tried adding a polycarb plate onto the churros to bridge the gap and make it smoother, however still wasn't actually sliding well on that to get the note into the robot for our interface with the shooter feeder on our elevator.

# Shooter High Fidelity

We had some cad mistakes that ended up slowing this prototype down fairly significantly, but we did make some progress.

![](https://i.imgur.com/kZaM02P.png)

Our printed hubs didn't have the right tolerances so we will have to print new ones for tomorrow, in the meantime we took some off of the other shooter wheels we have. We also have our lexan plates that will need to be cnced tomorrow for the shooter prototype, as we didn't get to that today.

# Climbing Mechanism Developments

So our original concept with the telescoping arms were hard to manufacture as we need the hook to end basically down by the top of our bumpers. The other major problem is it didn't have much height for actually grabbing the chain to climb. Having only a few inches of leeway for grabbing on would make the buddy climb very challenging, as well as last second hail mary climbs sort of impossible if we wanted to play some climb chicken. Mounting them rigidly was going to be tough, so we briefly went to a climber that was a double reverse 4 bar similar to some climbs in 2020.

![](https://i.imgur.com/MNdN4kp.jpg)

something similar to this which was sprung up, then winched down for the climb.

The problem we had with this is it would interfere with the shooter, and we would have to have dynamic code to avoid collisions between the climber and the shooter.

![](https://i.imgur.com/ZJyG06F.png)

The concept also had to be much narrower than we would like due to packaging reasons, which could have probably been resolved but it is coming down to crunch time a bit.

We eventually moved to a different climb concept inspired by 7407.

![](https://i.imgur.com/hbszVUQ.png)

This design would use our current elevator for launching anyways and dual purpose it for climbing. There is a passive hook to take the chain so we can re-extend for our trap score. We decided to go with this for now as it seems the most viable and simple for our current archetype.
# Motor Allocation

Here is our initial motor allocation.

1. Steering Front Left
2. Driving Front Left
3. Steering Front Right
4. Driving Front Right
5. Steering Back Left
6. Driving Back Left
7. Steering Back Right
8. Driving Back Right
9. Intake
10. Shooter Left
11. Shooter Right
12. Feeder
13. Shooter Pivot
14. Climber Left
15. Climber Right
16. Elevator 1
17. Elevator 2
18. -
19. -
20. -

# Blocky Cad for the day

We added our current climber concept + intake side plates from the prototype.

![](https://i.imgur.com/RCshSSn.png)

-Brennan