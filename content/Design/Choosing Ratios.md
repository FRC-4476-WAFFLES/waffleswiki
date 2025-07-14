# How to Select an Appropriate Gear Ratio

To select an appropriate ratio for a [[Mechanism]], we first need to set some baselines of what our mechanism should be able to do. Generally that comes down to two questions

- How much mass does it need to move?
- How fast does it need to move for a set common range?

## How Much Mass?

The simplest answer for some of these mechanism is simply how heavy is the thing you are trying to move? This can be solved by getting a [[weight estimate]] either through [[Solidworks]] or weighing actual parts on a scale (or a combination of both!).

## How Fast?

Part of the brainstorming process is setting time limits for how quickly you want an action for the robot to take. Some examples might be:

- Less than a second to move the [[elevator]] from ground to top
- Ball goes through the conveyor in 2 seconds
- Climber lifts robot within 3 seconds

This is going to drive how many [[motors]] and what kind of ratio you need.

## Process Notes

Start with one motor, then add as needed. Take a look at [[Choosing Motors]] for what motors are best for what application. If we can do the job with one motor that is preferable for a few reasons. One is it's removing a point of failure, you also don't have to wire an additional [[Motors|motor]]. Sometimes the robot will be stretched thin for available motor slots, and another [[Mechanism]] may need a motor.

If a task can be done at a higher reduction to increase torque, that is beneficial as you draw less current from the battery. This reduces the chances of a brownout, and makes battery depletion less.
# Design Calculator

We use [Recalc](https://www.reca.lc/) to do the math calculations for our [[Mechanism|mechanisms]]. Each calculation has a unique url that you can copy and save for reference later. Save these urls and put them in [[Slack]] for future reference.

# Example Calculations

## Conveyor

### Restrictions
- Empty conveyor in 0.5 seconds
- Conveyor is 40 inches long

### Process

We are going to select our motor first, starting with one motor. We default to the [[Kraken X60|Kraken]] for this based on [[Choosing Motors]].

Next we set our travel distance, which in this case is 40 inches, as that's how long our conveyor is.

In this example we are using two inch diameter rollers. This could be any diameter, and generally for conveyors the size of rollers should be determined by making the smallest possible rollers while not having any dead spots/making it easy to assemble.

Now looking at the time to goal field we adjust the time to goal till we hit our goal time. We want a ratio that just barely hits our time goals, as we want to maximize the torque available in the system and minimize the current draw on the robot.

![](https://i.imgur.com/W3f79fG.png)

You can see the actual calculation using [this link](https://www.reca.lc/intake?drivetrainSpeed=%7B%22s%22%3A14%2C%22u%22%3A%22ft%2Fs%22%7D&motor=%7B%22quantity%22%3A1%2C%22name%22%3A%22Kraken%20X60%2A%22%7D&ratio=%7B%22magnitude%22%3A7%2C%22ratioType%22%3A%22Reduction%22%7D&rollerDiameter=%7B%22s%22%3A2%2C%22u%22%3A%22in%22%7D&targetTimeToGoal=%7B%22s%22%3A0.25%2C%22u%22%3A%22s%22%7D&travelDistance=%7B%22s%22%3A40%2C%22u%22%3A%22in%22%7D)