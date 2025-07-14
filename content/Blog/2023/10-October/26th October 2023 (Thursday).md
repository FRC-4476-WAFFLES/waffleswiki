---
tags:
  - blog
  - design
  - CAD
  - Intake
  - 3Dprinting
  - driveteam
  - strategy
  - FEA
date: 2023-10-26
---
# 254 2023 Tech Binder Review

Just wanted to document a couple cool things 254 did in 2023 that may apply to us at some point in the future. Some of this is documented in their [tech binder](https://media.team254.com/2023/10/90bc07c6-2023-Tech-Binder-V6.pdf), some in their [Chief Delphi](https://media.team254.com/2023/10/90bc07c6-2023-Tech-Binder-V6.pdf) thread

## Cube Intake

![](https://i.imgur.com/va27B9c.png)


Very cool cutout into the [[Polycarbonate]] which was a light weight smart way to power the cube [[Intake|intake]] in and out. It's made out of two milled out pieces of 1/4" polycarb plates at 10DP. Not sure we could mill the same thing, but we could do a three stack of polycarb instead potentially. Then it's powered by one internal shaft going across the whole length of the robot to power both sides

## Printed Pulleys

> [!quote] [Torrance on Chief Delphi](https://www.chiefdelphi.com/t/team-254-presents-2023-breakdown-technical-binder-code-q-a/443167/6?u=brennanb)
> – This year we tried to use more aluminum pulleys because we had the teeth shear off in a printed 18T 5mm HTD pulley in our 2022 Serializer at Chezy Champs, and it was crazy hard to disassemble and swap.  
– When printing a pulley, we printed in Solid Fill and additionally added ~qty4 1/16" holes for [shear pins](https://www.mcmaster.com/90145A419/) to go between the layers

Interesting that they had teeth fail with solid fill, and then had shear pins support which we currently don't do. We haven't had teeth fail, just the flanges for holding the [[Belt]] on the actual pulley break of making the pulleys un-usable. Does make me a bit more aware that we want to test high load/hard to replace printed [[Pulleys]] extensively before going into a competition with.

## Hall Effect Sensors

> [!quote] [Torrance on Chief Delphi](https://www.chiefdelphi.com/t/team-254-presents-2023-breakdown-technical-binder-code-q-a/443167/6?u=brennanb)
>– Hall sensors are wired as a limit switch to the Falcons and serve to zero the joints  
– For the floor [[intake]] and Laterator they are on the retracted hardstop which is the starting pose  
– The elevator starts midway up with a little kickstand for faster initial auton placement, but its Hall is still at the bottom of travel so only is triggered in a floor cone pickup pose or if we lose our encoder position and want to rezero  
– Forks carriage triggers a hall when all the way climbed, to tell the motor to stop pulling

Wiring [[Hall Effect Sensors]] directly to a [[Falcon 500|falcon]] wasn't something I was even aware of. This seems like a nice way to do it, and I assume the [[Kraken X60|kraken]] is also capable of doing this, but we should check!

Big fan of hall effects for zeroing things because there is no contact. Lets use them in 2024!

# Drive Team Filming

I want to film behind the glass for stemley and all events in the future. Team will have to invest in things to make this happen for every [[match]] so we can review it strategically and work on our communication within the [[drive team]].

-Brennan

# Pocketing Patterns

**TL;DR:**
Vertical load: Square pocket great, 2056 style and thin wall good
Horizontal load: Thin wall fantastic, 2056 style and square pocket okay
Compressive load: Thin wall great, 2056 style and square pocket good
Keep in mind that thin wall tubing is harder to get, pocketed extrusion takes time to pocket.

Inspired by the pocketing on my 2056 redesign project, I ran a few basic FEA tests on 2x1 aluminum extrusion with different lightening techniques. I tested for deflection and stress on 6 pieces of 11" long 2x1 extrusion; 4 pocketed 0.1" tubes, 1 plain 1/16 tube, and 1 plain 0.1" tube. The mass of these tubes are 0.377, 0.387, 0.380, 0.399, 0.386, and 0.600 pounds respectively.

![](https://i.imgur.com/Hlg1PlP.png)
2056 style, square, 4476 style, circular, thin wall, regular.

In a vertical load test, the back face of each extrusion was set as a fixture and a 1000N load was applied on the front face pointing directly downwards. Below are displacement and stress results. 

The displacement increase/mass reduction of each lightened tube was calculated using the formula `d / (M - m)`, where d is the measured displacement at the end of the tested tube, M is the mass of the 0.1" plain tube, and m is the mass of the tested tube. The values are:
==6.64, 6.18, 6.96, 8.39, and 6.67== mm/lb respecitvely (lower is better, sorry for the weird units).

Also worth mentioning is that amongst the pocketed tubes, the square pattern showed the least amount of stress at the corners, even though all fillets are done to the same radius. Lower stress means a lower chance of permanent deformation/failure.

![](https://i.imgur.com/MJFmexs.png)
![](https://i.imgur.com/WpVYbYZ.png)

A horizontal deflection test was set up in a similar way to the vertical load test, but a 500N load was applied pointing directly sideways instead. Below are displacement and stress results.

The displacement/mass reduction ratios were calculated for this test as well, and the values came out to be:
==18.40, 18.46, 19.07, 19.9, 9.83== mm/lb respectively (again, lower is better).

The square pattern also shows the lowest stress amongst the pocketed tubes in this test as well.

![](https://i.imgur.com/wGnc6u6.png)
![](https://i.imgur.com/q7voQM2.png)

A horizontal deflection test was set up in a similar way to the vertical load test, but a 500N load was applied pointing directly into the tube at the top and bottom edges instead. Below are displacement and stress results.

The displacement/mass reduction ratios were calculated for this test as well, and the values came out to be:
==11.56, 12.15, 14.00, 12.78, 9.97== mm\*10^-2/lb respectively (again, lower is better).

The corners in the 2056 style pocketing saw the lowest amount of stress.

![](https://i.imgur.com/CfhLINO.png)
![](https://i.imgur.com/dLv5oyB.png)

In terms of pure performance, the most impressive tubes were the equilateral triangle pocketed, square pocketed and thin wall tubing. Circular pocketing is very quick to CAD but performs very poorly, and 4476 style tubing performs poorly (and looks bad, imo). Good discovery to make before we carry our pattern over to future seasons.

Vertical load: Square pocket great, 2056 style and thin wall good
Horizontal load: Thin wall fantastic, 2056 style and square pocket okay
Compressive load: Thin wall great, 2056 style and square pocket good

More testing will be done to test how performance of pocketed tubing changes when the pocketing pattern is altered slightly (webbing width, top & bottom thickness), but maybe after the 30% midterm I'm about to have in about 18.5 hours :))

\- Brandon