---
tags:
  - design
---
# Newton's Laws

These are the fundamental laws behind classical mechanics, which dictates how most of our day to day objects act and interact.

1. An object will remain at rest or in uniform motion unless there is an unbalanced force acting upon it
2. F = ma (Where F is the force on an object, m is the mass of the object, and a is the acceleration of the object)
3. Each force acting on an object has an equal and opposite reaction force acting on the other object
# Force

Newton's laws talk a lot of about force, but what actually are they?

A **force** is a push or pull on an object that can cause acceleration (can cause things to start or stop moving, or move in a different direction. More on this later).

Some examples:
- Applied force (a push)
- Tension force (a pull, usually through rope or similar)
- Gravitational force (the force that pulls all objects towards each other)
- Normal force (typically the reaction force that supports Newton's 3rd law)
- Friction force (resists motion between touching objects)

A force is a vector, meaning it has a direction associated with its value. If there are multiple forces on the same object, the forces can add towards or subtract from each other depending on their directions. If the forces cancel out, they are balanced and so according to Newton's 1st law, the object will remain at rest or in uniform motion!

(insert fbd)
# Kinematics

In order to understand what acceleration is, we also have to understand displacement and velocity.

**Displacement** is the difference in position between where an object starts and where it ends. Unlike distance which doesn't specify the object's direction of travel, displacement is a vector and changes based on the direction you're measuring it in. For example:
- If a robot starts right in front of your alliance wall and ends up at the exact other end of the field, it has a displacement of 54ft in the forward direction. When looking at the robot in the backwards direction, it has a displacement of -54ft. The robot also has a sideways displacement of 0ft.
- In an elevator system with 28in of travel, if the carriage starts at the bottom and ends at the top, it has an upwards displacement of 28in, a downwards displacement of -28in, and a sideways displacement of 0in.

**Velocity** is the change in displacement over a certain amount of time. In the same way that displacement is similar to distance but specifies a direction, velocity is similar to speed but specifies a direction. For example:
- If the robot drives at 20ft/s forwards for 1 second, it will end up with a 20ft forward displacement.
- If the robot drives at 10ft/s backwards for 2 seconds, it will end up with a -20ft forward displacement (which is the same as a 20ft backwards displacement).
- If the robot drives at 1000ft/s (holy moly) to the right for 1000 seconds (woah mama), it will end up with 0ft of forward displacement.
- If a carriage takes 2 seconds to reach 28in of upwards displacement, it has an average velocity of 14in/s upwards.

Now, acceleration. **Acceleration** is the change in velocity over a certain amount of time. It also specifies a direction. For example:
- If the robot takes 1 second to reach 20ft/s, it has an average acceleration of 20ft/s^2
- If an apple on the Earth's surface is dropped with no support, it will travel at 9.8m/s after 1 second and at 19.6m/s after 2 seconds. It has an acceleration of 9.8m/s^2 downwards.

Acceleration due to gravity on the Earth's surface is always 9.8m/s^2! This is commonly written as the g constant (g = 9.8).

Combine this with Newton's 2nd law, the gravitational force for all objects on the Earth's surface is Fg = mg.
# Torque

If a force is a push or a pull that causes linear acceleration (F = ma), torque is a twist that causes angular (rotational) acceleration:

tau = I alpha

Where tau is the torque applied, I is the moment of inertia (essentially how hard the object is to spin, see below section), and alpha is the angular acceleration.

Torque is extremely common in our day to day life. You applying torque on every door you open, your car's engine applies torque to the wheels to get them to spin, you apply torque every time you open your laptop. Muscles in your body apply torque on each joint that you move!

Often times, torque is a result of a force (eg. opening a door). The formula to find the torque from a given force is:

tau = Fdcos(theta)

Where tau is the torque, F is the force applied, d is the distance between the applied force and the pivot point (aka. moment arm), and theta is the angle between the applied force and the line between the applied force and the pivot point.

This formula may be confusing to some, but the important thing to understand is that given a certain amount of force, the torque is maximized when the moment arm is big and when the force is perpendicular to the moment arm. With this in mind, you'll start to see how almost everything that moves on a robot moves as a result of torque.

(insert photo for comparison)
# Moment of Inertia

As mentioned earlier, the moment of inertia can be understood as how hard it is to get an object to spin. But how do we know what this value is?

The moment of inertia of an object depends not only on how much mass it has, but also on how far that mass is from the axis of rotation. Think about it this way - if you were holding a hammer in each hand, would it be easier to spin around quickly when your arms are stretched out or tucked in? It would be easier to spin when the hammers are close to your body, even though you have the same amount of mass in both scenarios!

You're not expected to know how to manually calculate for the moment of inertia for any object (doing so requires math skills like 2D integration and working in polar coordinates), but there are formulas for common shapes:

(insert formulas)

When designing joints on FRC robots, lower moment of inertias are generally better. This means keeping all heavy components closer to the pivot point (eg. motors, heavy wheels etc). However, there are places where you want a higher moment of inertia. An example of such place is for the shooter wheel, as you want it to decelerate as little as possible when it comes into contact with a game piece.
# Second Moment of Area

Similarly to how the moment of inertia of an object measures the amount of mass and the distance between that mass and the point of rotation, the second moment area of a shape measures the amount of area and the distance between that area and the central axis. 