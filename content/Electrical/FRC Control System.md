By the [[Game Manual]], every FRC robot must have the same control system. This is the core of the operation of every robot. There are many components such as Batteries, [[Roborio]] , wiring and much more. There are various vendors for different components of the control system. 

## Components
[[Roborio]] : The central computer of the robot. The [[Roborio]] is the only allowed robot controller for [[FRC]] robots. It is made by National Instruments .This is where the code will be downloaded and ran. It will take all the inputs from robot and [[Driver]]/[[Operator]] and calculate the outputs. It has many connections as listed here: USB, Ethernet, Digital Input/Output, Analog Input/Output, [[Radio Signal Light]], [[PWM]], SPI, USB-B, I2C, RS-232, SPI and [[CAN]].

[[Radio]]:This is how the robot communicates with the [[FMS]] and the [[Driver]]/[[Operator]]. Until the 2025 Season, all teams must use the same OM5p radio. It has 1 Power Over Ethernet(PoE) input, 1 Barrel Jack and 2 Ethernet outputs. It will connect to the [[Roborio]] by an ethernet that may or may not be PoE powered by a [[VRM]] or [[RPM]].  It can also be powered by a standard barrel jack that is connected to the 12V/2A on the VRM, or a small fuse on the PDH. Network Table devices such as [[LimeLight]] may be plugged into the output ethernet jacks for video and coordinate transmissions. 

Main Breaker 120A thermal breaker separates the battery from the [[PDH or PDP]] .  It acts as the main on/off switch for the robot

[[PDP or PDH]] 

Actuators

[[RSL]]

Digital Sensors

Analog Sensors

[[Pneumatics]]



## [[CTRE]] Wiring
![[CTRE Control System.png]]
## [[REV]] Wiring
![[Rev Control System.png]]