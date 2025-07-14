---
tags:
  - elevator
  - assistingteams
  - debugging
date: 2023-10-24
---
Had a call with team 5719 trying to help them out with their assorted robot issues prior to STEMley! Always a good experience to help out other teams and gives us the chance to learn something from other teams systems.

One thought I had was to implement a better systems check any time the robot has gone through transport. Generally we do give the robot a look-over, but journeys in the trailer can always cause some things to come unplugged in ways that others haven't.

Also a good reminder to go over what the lights mean for any assorted [[Motor Controller]] (and honestly, things like the [[Roborio]] and [[PDH]] as well).

[WPILib documentation for lights](https://docs.wpilib.org/en/stable/docs/hardware/hardware-basics/status-lights-ref.html)
[Spark Max Lights and What They Mean With Fun Animations](https://docs.revrobotics.com/sparkmax/status-led)

Hopefully we got them up and running - looks like some issues with the ribbon cable on the [[NEO Brushless V1.1]] motor that they had been using (which is an annoying but common issue with the first gen of the [[REV]] products). 

Another design choice they had made was an [[Elevator]] with a [[Shifting Gearbox]]. The [[Pneumatics]] had seemingly fired so it was stuck in second gear, which was partially contributing to their elevator issues? Not something I think we would often have a use for, but some 2018 robots used shifting gearboxes on their arm to activate 'climbing mode'. 

Also a reminder to keep git up to date if for no other reason than version control. I'm still learning how to use it and am on the struggle bus sometimes but it is useful.

-Taegen

