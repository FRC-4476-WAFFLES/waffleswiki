---
tags:
  - Solidworks
  - CAD
  - design
  - Intake
  - arm
---
# 4499 Robot Notes

## General Construction Notes

- 4499 makes use of a lot of tapped holes, which help eliminate much of the frustration that can come with trying to hold a wrench in place for nuts during assembly. Most tapped holes are in 1/4" aluminum plates
- A lot of metal parts on this robot are half pocketed, meaning metal sheets and tubing faces are lighted most of the way through but some material is left to add quite a bit of rigidity over fully pocketed parts. All half pocketed parts on this robot leave 1/16" of material
## Intake Rollers

To save weight, the designers went with a screw end live axle intake roller for their cube holder.

![](https://i.imgur.com/MGrD9lX.png)

This is another variation of the design outlined in the [9th of November blog](https://wiki.wafflesrobotics.com/Blog/2023/11-November/9th-November-2023-(Thursday)#screw-dead-axle), where a screw acts as an axle on each side of the roller. However, the big difference is that 4499 put a fixed nut in the pulley plug where the shoulder screw's threads would mesh.

With this change, they didn't need to deal with the unintuitive assembly order that the 254 and 1678 style roller required as the screw could be inserted and tightened once the roller was in place. However, the downside is that this is now a live axle roller and bearing retention becomes an issue again. 4499 also specifically had issues with the plug portion of the pulley plug breaking due to its thin walls and used an adhesive as a quick fix.

## Worm Gearbox

Instead of using convectional planetary or spur gearboxes, 4499 bought a worm gearbox rated for high speed and high load applications off Amazon. Worm gearboxes only allow power to be transmitted through it one way (motor can drive the arm, but the arm can't drive the motor), so this arm turned out to be very stiff. This gearbox style was chosen to eliminate any potential need for an extra braking system.

![](https://i.imgur.com/I1UuIZn.png)

The gearbox was originally mounted on a sliding plate that could be adjusted to tension the chain, but the plate ended up being a weak point and was later swapped out for a solid plate instead. They then moved to an inline chain tensioner.

# Wrist Slip Gear

To make sure they weren't skipping belt teeth on their wrist mechanism, 4499 implemented a slip system on their wrist powertrain that can transmit power, but gives way when there's an excessive external force. It uses two metal (I believe steel and aluminum) parts that clamp around a portion of a modified spur gear. The plates are held together by screws with spring loaded washers to keep them pressed against each other and the gear. The friction between these plates and the gear is enough to transmit the torque required to power the wrist, but slips when the intake is run directly into a wall. Tension on the plates can be adjusted by tightening or loosening the screws between the two plates.

![](https://i.imgur.com/R0fhTTU.png)

# Arm Zombie Axle

It's generally bad to use a live axle hex shaft to transmit torque through a heavy arm, so most teams use a dead axle setup where the central shaft doesn't spin and instead the torque is transmitted straight to the arm (sprocket/pulley directly attached to arm). 4499's setup is somewhere in the middle, where the torque is transferred straight to the arm but with the axle attached and spinning. There's a lot of discussion on what this setup should be called, I'll settle for calling it a zombie axle.

![](https://i.imgur.com/MMV3Kh7.png)

The sprocket transfers torque to the arm through bolts that go through the sprocket, a 3D printed spacer block, and screw into a clamping block that not only clamps the outside of the arm, but also has tabs that fit into mating slots on the arm. The axle rotates with the arm due to friction so that it'd be easy to have an encoder read the rotation of the axle. The axle itself is a 1" hollow round rotating inside bushings that are press fit into a bracket fixed on the frame.