---
aliases:
  - robot intake
  - intake
  - intakes
  - Intakes
---
Intakes are a subsystem on pretty much every robot where the purpose of the subsystem is to acquire game pieces and store them in the robot. Since intakes have such a broad definition, there are a large amount of different types of intakes.

## General Intake Design Guidelines

- Try to use rollers/wheels over pinching/grasping [[Mechanism|mechanisms]]. Rollers almost always are more forgiving for alignment to pick up a game piece.
	- When using rollers, make sure there are no dead zones where a wheel is not in contact with the game piece.
- Read the intake section of [this](https://wiki.wafflesrobotics.com/Blog/2023/11-November/9th-November-2023-(Thursday)) blog for a guide on some roller types.
### Choosing an Intake Ratio

- Surface speed of roller at least 2 * robot max speed
	- If driving towards an object at max speed, you still need to be able to have net positive intaking speed
	- The 2* or more is needed because with a single top roller, the object will be rolling, so middle of object has speed V getting pushed, 0 at carpet (assuming in worst case no slip condition) and 2*V at top of object
	- Surface speed = motor free speed RPM * 80% (efficiency) * gear ratio * roller circumference (length units) * conversion factors for units
### Rollers and Compression

- Maximize grippiness (contract friction) through all methods to maximize energy transfer, and thus intake speed and reliability
	- Friction = Coefficient of Friction * Normal Force between objects
	- Find the most grippy pair of materials, such as rubbers or fancy grippy tapes, to increase coefficient of friction
- Have enough normal force to lift object against gravity and pull in quickly
	- Normal force needs to be generated between roller-object-ground, roller-object-bumper, or roller-object-something
- If object is rigid (examples: 2019 hatches, 2018 cubes, 2017 wiffle balls) you need compliance/compression either in the mechanism (pivoting point allow floating wheel/roller and springs/pneumatic-pressure generates squeeze force) or in the wheels/rollers ([[Compliant Wheels]], thick rubber surfaces).
- If object is compliant (examples: most balls, 2023 cubes/cones) then you can have a rigid roller and instead compress the object
- Don't have too much normal force because it increases resistance/drag which can slow system down and make it drawing more power, this is why maximizing grippiness through material selection is optimal
### Intake Size

- Maximize intake area to simplify [[driver]]/[[autonomous]] skill required
	- Ideally intake is as wide as entire robot, which usually means its better to pull object over bumper and then center/serialize inside robot
	- Also means intake has to deploy outside bumper perimeter which leads to point building robust intakes
### Build Robust Intakes

- Build robust intakes
	- Use 1/4" [[Polycarbonate]] plates for good mix of stiffness and toughness (bend then spring back without cracking)
	- Big plates with plenty of material around holes. Ideally small holes, that's why the dead axle roller [[design]] is so good, you only have a bolt hole in the plate
	- Have spares and design-for and practice quickly repairing
	- Use [[Sensors]]
		- [[Hall Effect Sensors|Hall effect]] sensors to zero motor driven deploy
		- Beam-break sensor (ex. retro reflective laser) to know that object is in robot and automatically trigger intake to stow, elevator to move, etc
		- Color sensor to detect multicolored game objects (ex. 2022 balls)
### Intake Indexing

Regularly intakes will have to index multiple pieces, or direct game pieces to a specific place in the robot to be singularized (IE. Intake is multiple game pieces wide, but needs to narrow down to one game piece wide)