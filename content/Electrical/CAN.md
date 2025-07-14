---
aliases:
  - canbus
---

A Controller Area Network more commonly known as CAN bus, is a communication Protocol used in many devices in the 21st century. A CAN bus connects a unlimited number of devices by 2 wires. The wires are generally coloured Green and Yellow. Yellow represents the High signal, while Green represents the Low signal. The secret to have so many devices connected on the same network is the baud rate and bit construction. 

## FRC Usage

In [[FRC]], CAN is one option for actuator control. Most devices such as motors and sensors have the option to connect to the CAN bus. The [[Roborio]] is the "head" of the network and will output/input all commands to change the operation of the robot. 

## Network Setup

For a network to function properly, there must be 120Ω resistor at every end of the network. Most devices in that are [[FRC]] legal already have the resistor inside them, such as the [[Roborio]] , a [[Falcon 500]], or the [[PDH]]. This simplifies the wiring for those who are assembling the system. 

In the [[FRC Control System]], there are some rules for the CAN network. The CAN network must be terminated at the [[Roborio]] and the other end at the [[PDH]] or [[PDP]]. There is an exception if [[Pneumatics]] are being used (insert alternate description here). All other devices must be somewhere in between the two terminations. 

### Network Types

There are various different ways to setup a CAN bus. There are topologies that can be used that offer different advantages. The standard (often expected by your local friendly [[Robot Inspector]]) configuration is a "daisy-chain/line" topology, however there are specific use cases where star or ring configurations are better.

### Star



### Ring


### Line/Bus/Daisy-Chain

Identical to series configurations for [[Electrical|electrical]] purposes, all of your devices are connected directly to one another, so there is an 'in' and an 'out' of the bus.

This means that the CAN wiring should usually start at your [[Roborio]] and go into and out of each device successively until finally ending at the PDP. It is important to note that any devices using a [[CANivore]] must be in a daisy-chain.

![](https://i.imgur.com/M3kjZym.png)

