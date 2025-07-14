---
aliases:
  - elevator
tags:
  - CAD
  - design
  - elevator
---
# What is an Elevator?

An elevator is a linear extension mechanism generally used to move game pieces and/or robot mechanisms vertically. They are usually built from 2" x 1" extrusion and small bearings.

Some basic elevator terms:
- Carriage - the last moving frame which travels the greatest distance, is usually what manipulators (arm, intake etc) are mounted to
- Rigging - the system powering the elevator's stages
- Stages - a moving subassembly, usually in the shape of a frame (includes the carriage)

![](https://i.imgur.com/gPY1oxv.jpg)
## Single Stage Elevator

Single stage elevators are very simple to build, as the carriage can slide directly on the stationary base frame and can be powered with a single length/loop of chain, belt, or rope.
## Multi Stage Elevator

Multi stage elevators add a lot of complexity, but are required if the carriage needs to travel greater distances (needs to go higher than the top of the base frame). There are two ways of rigging multi stage elevators, Continuous and Cascade. We'll dive into how each works, but you can visualize the motion of each system by increasing the number of stages in [this elevator visualizer](http://www.competitionrobotparts.com/elevator-visualizer/).
### Continuous Elevator

Continuous elevators use a single run of rope to pull the carriage up, and another single run of rope to pull the carriage down. The <span style="color:green">pull-up rope</span> winds around a powered drum, passes over a series of passive pulleys at the top and bottom of each moving stage and attaches to the carriage. The <span style="color:red">pull-down rope</span> simply has to wind around a powered drum and attach directly to the carriage.

![](https://i.imgur.com/gdvEC4E.png)

The stages of a continuous elevator move one at a time, usually with the carriage moving first, then the second to last stage, and so on. This keeps the center of gravity as low as possible for as long as possible, but introduces some force inconsistencies which have to be accounted for in code. To make sure the stages are raised in order, some teams use stronger magnets or constant force springs to hold the bottom stages down.
### Cascade Elevator

The motor on a cascade elevator only directly powers the first stage. The subsequent stages are powered by passive <span style="color:green">pull-up</span> and <span style="color:red">pull-down</span> rope segments (when the first stage gets pulled up directly by the motor, the pulley at the top of the first stage pulls the second stage upwards at twice the speed and with half the force). Pull-up and pull-down rope segments are commonly combined into a single loop of rope, and the first stage rigging can be achieved with just a single loop of chain/belt to reduce complexity (e.g. [ThriftyBot's elevator kit](https://www.thethriftybot.com/products/thrifty-elevator-stage-kit?variant=45951434162475))

![](https://i.imgur.com/quXspJ7.png)

Since all stages move at once, the motion is smooth and predictable but the center of gravity would be higher at moderate elevator heights.
# Miscellaneous Elevator Things 

## Kickstand

254 created a "kickstand" which was a simple 3d printed hard stop that sprung out of the way after the carriage moved out of the way. This allowed them to start the match at a different height which was closer to the scoring height for [[2023 Charged Up]]. You can find more about it [[28th October 2023 (Saturday)#254 Elevator Kickstand|here]].

![](https://i.imgur.com/MW8skOh.png)
![](https://i.imgur.com/GRsihbq.png)