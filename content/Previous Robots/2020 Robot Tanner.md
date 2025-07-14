---
aliases:
  - Tanner
date: ""
---
# About

## The Game

## Team Abilities
In terms of team members for the 2020 season, we had 4 strong CAD students and experienced [[Mentor|mentors]] for [[design]], mechanical, and [[electrical]].  We had [[Sponsor|sponsors]] for laser cutting for metal and waterjet for [[Polycarbonate|lexan]] parts.  This was the first year that we had structural 3D printed parts (PLA), and our second year of using a [[LimeLight]].

## Robot Name

## Fun Lore
none

# The Robot

![Tanner 2020](https://i.imgur.com/S4GuVV4h.jpg)

The robot had a west coast drive with a [[ground pickup]] on a virtual four bar, feeding into a funnel for indexing with a 5-ball capacity.  It had a Limelight for vision tracking and could score in the high goal, using a hood with two positions.  It was short enough to go through the trench.  The climber had a virtual four bar deployment with a winch.  It had an [[electrical]] box to house most [[electrical]] components.
## Mechanical [[Design]]

### [[Drive Train]]

The West coast [[drive train]] had 6 wheels with a centre drop and ran on 4 [[Falcon 500|Falcon]] [[motors]].  This was the first time we used [[brushless motors]] and our first experience with [[Falcon 500|Falcons]].  The standard 6" high grip wheels from [[AndyMark]] were used.  A metal baseplate was used for the first time.

During a practice session, when the robot was spinning, the battery was ejected from the robot and caused backdriving in the [[Falcon 500|Falcons]].  This fried some of the [[electrical]] components ([[LimeLight]], VRM, PCM).  This issue was later fixed in a firmware update.  The bolts on the output shafts of the [[Falcon 500|Falcons]] required [[Loctite]], which was difficult to perform maintenance for due to small clearances, and required significant disassembly.

During our competition, we did not have any issues with the drivetrain.

![500](https://i.imgur.com/8zC4D5r.png)

### [[Intake]]

The intake deployed via a piston-actuated virtual four bar and had 3 rollers; the first had [[AndyMark]] compliant wheels and the following two were ABS pipe rollers with 3D printed hubs.  The rollers were powered by a bag [[Motors|motor]].  The side plates were made of [[Polycarbonate|lexan]] to absorb impacts and they were spaced using 3D printed spacers.

![500](https://i.imgur.com/kJpjpjl.jpg)

There were no dead zones in the geometry, but we found that the compression was too high (or a stronger [[Motors|motor]] was required) when doing high speed pickups and the balls would make contact with the bag [[Motors|motor]].  We had grip on the first roller for better pickup and at different heights depending on where balls were on the field, but found that the subsequent rollers did not need additional grip.  The shafts went through both of the rollers for rigidity, but for similar designs in the future, a dead axle [[design]] could be tried.  

We had issues with overtightening the bolts connecting the [[Polycarbonate|lexan]] side plates, causing the spacers to crack and need replacement.  The deployment worked well, but we would increase the robustness of the metal used in the four bar, as the metal plates bent with use ([[intake]] impacting with walls).  The turn buckles for the chain tension on the virtual four bar worked well, but would loosen over time (see second image in the funnel section).  The [[intake]] also relied on the bumpers as a hard stop, but the bumpers were not made with high precision so the intake geometry needed to be adjusted. The bearings in the intake would also fall out during use occasionally. In the future we should have either better bearing retention, or more rigid lexan intake plates so they don't bend and push the bearings out during collisions with the intake.

The intake could also jam if a ball was not fully contained in between the lexan side plates. The 2020 game piece was extremely grippy, and it wouldn't center into the intake well, causing the ball to compress and get stuck in the wheels.
### [[Funnel]]

One side of the funnel had a polycord [[Belt]] to agitate the balls and push them into the conveyor.  It went from a width equivalent to two balls wide down to one ball wide.  Three balls could be stored in the funnel at a given time.

**![](https://lh7-us.googleusercontent.com/EmNaPW8II_FEP1XfC0ZJKrua3SIpywaO89koaoWLV5bH5QV4PmeA0YxRKJHUwXzcX9M4LSKUJWVGhrBZTHCOvm4zwyGrfM3IqfHIOl7-F1NYoKDHV3aKk8KNMyVc_JPL4m5i6qIl_XeKxB2TbC3TYA)**

We had issues with balls falling out because there was no [[Polycarbonate|lexan]] top in the actual version, due to weight limitations.  Metal [[Pulleys]] were originally used, but were swapped to crown pulleys to avoid damaging the balls.  Extra lexan was added to the [[intake]] to better guide the balls into the funnel and prevent balls from falling out.  The funnel mounting [[design]] was not optimal for maintenance, as the lexan blocked access.  The plate on the top side of the polycord [[Belt]] would dig into the ball and limit proper contact/indexing.

![500](https://i.imgur.com/jXgoMAV.jpg)

### [[Conveyor]]

The conveyor fed the balls indexed by the funnel into the [[shooter]] using polycord [[Belt|belts]] on 3D printed crown [[Pulleys]], and it was powered by another bag [[Motors|motor]].

**![](https://lh7-us.googleusercontent.com/nz2VGuPecg2qrlZmvF_oTGfHTbIrVFN12GCzei8MEqymCN0tXBK9-SkXvc2RPGCkGp-XE4c0QfFLZ9Bd9NIodiryNyW4gKBdEhHuwud7dmOKiIc-ZQsV5-DMtGVJCjqrDcCU03s7sA1c6zVM5LEzkQ)**

The transition from the funnel to the conveyor was not fully planned, and thus there were issues with geometry and dead spots.  The crown [[Pulleys]] were not perfectly aligned, causing the polycord [[Belt|belts]] to slip off frequently.  Ball jams frequently occurred in the conveyor.
### [[Shooter]]

The shooter was powered by 2 neos. The hood was 3d printed pla, and had slots in it to have two positions for a wide range of shooting locations. The hood was powered by a single acting piston, defaulting into the closer range. The shooter also had a [[LimeLight]] to align to the goal, as well as a general range finding algorithm for either a long range shot from the trench or a closer initiation line shot. The shooter also had an acceleration wheel to help minimize the load on the main flywheel and maintain flywheel fire rate.

The shooter itself was quite rigid and had a reasonable firing rate. Generally it was more accurate than many shooters in the field, and had reasonable inner percentage rate. There was some left/right inaccuracy that we saw due to inconsistent loading of the power cells through the shooter. This was because the actual feed of the shooter had some range left right where the ball could enter the shooter and thus the output saw that same error as well.

For the robot to shoot we would back off the conveyor, kicker, and flywheel to give some gap for the shooter to spin up, then it would have the flywheel spin up. Once the flywheel was within range, the kicker and conveyor would launch the balls.

The shooter also had some jamming issues with the powercells, where either two balls would get stuck compressed together near the feeding wheel, or sometimes the power cell would get stuck in-between the feeding wheel and the flywheel. We never fully determined the cause of this, but we had a few potential ideas.

1. Part of the de-jam code actually jammed it by reversing
2. The logic for slowly indexing balls in sequence failed, and the powercell bypassed the feeding wheel and made contact with the flywheel that jammed balls in
3. Some difference in grip between the polycord belting and the wheels causing the ball to get stuck

We also started designing a second revision for the shooter that had a sheet metal hood with rack and pinion adjustability for the hood. The primary goal of this was to be able to shoot from the protected zone right in front of the goal. Our two position hood didn't have the ability to do this as the hood would need to be at a much steeper angle. We never ended up building this however as [[FIRST]] events shut down due to covid.
### [[Climber]]

The climber was a combination of two mechanisms; a virtual four bar hook delivery system, with a winch [[mechanism]] to lift the robot. To move the system the winch and the hook deploy had to move in union.
#### Hook Deploy

The hooks were stored on the end of a virtual four bar system to get the height to lift the hooks to the climbing bar. The deployment was powered by a singular [[redline]] motor
#### [[Winch]]

The winch used rope run off of a spool on either side of the robot. This spool had a very high reduction gearbox on a neo 550. The 550 was chosen specifically because it was the only motor that fit within the space requirements.

Originally the winch had planned pneumatically actuated ratchet wrenches that would prevent back drive. These were removed later because the back drive of the motors thru the gearbox was limited enough that the robot would stay up for long enough.
## [[Software]]

For aiming the limelight looked at the area of the target in a wide view, and then tried to center the middle of the target to the center of the robot for aiming towards the middle of the goal. The limelight would also automatically switch to a more zoomed in version of targeting if it detected a long range shot (low area target.) Depending on the area that it saw on the targeting, the flywheel rpm would fall into 3 different buckets of range (far shot, mid shot, close shot) This would give the shooter the approximately correct rpm to make shots.


## [[Electrical]]
is so prettyyyyyyyyyyyyyyyyyy
![500](https://i.imgur.com/lnR6mSA.jpg)



## Key Lessons Learned

- Dealing with multiple foam dodgeballs in a robot requires extreme care to index and pick up.
- 3d Prints were stronger than we thought, and can be used frequently in structural parts
- It's super important to have good packaging with different subsystems and get different subsystems talking to each other early.
- Blocky cad for marking out subsystem sizes is super useful.
- Back driving motors at huge speed can destroy electronics!

# Performance

## [[Awards]]
