---
tags:
  - blog
  - CAD
  - design
  - Intake
---
# Topics:
- Custom Gearboxes
- Roller Styles
# Custom Gearboxes

There are two main ways of doing gearboxes in FRC; COTS planetary gearboxes and custom spur gearboxes. Historically, 4476 has tended to use planetaries as they're adjustable and easy to design for, but moving forward (especially on precision high load mechanisms) it would be nice to make use of some spur gearboxes because they're less fragile, have less slop, and can package nicely in some cases. It is also easy to design them to 

![](https://i.imgur.com/SWzXn66.png)


Spur gearboxes have less slop than planetaries, but there's still some play in the interfaces between gears and hex shaft as well as between separate gears.

To reduce play between the gear and the hex shaft it's on, many teams used [shim tape](https://www.mcmaster.com/1143N23/) to fill tolerance gaps, while others used [Loctite 609](https://www.henkel-adhesives.com/ca/en/product/retaining-compounds/loctite_6090.html) to do the same thing. Of these two options, shim tape looks like the more realistic approach for us as a heat gun isn't required to soften Loctite when performing maintenance. 4414 goes over their shimming process [here](https://www.chiefdelphi.com/t/team-4414-hightide-2023-robot-tsunami/428584/231?u=bdon).

To reduce play between gears, a few teams take away 0.002" from the standard distance between axles so that the teeth mesh better. However, this method requires a run-in period where the gears are run at speed without grease for a few minutes to wear the teeth in a bit so they would run smoother. On the other hand, some teams will add 0.003" to their gear center distances to make their gearboxes run smoother. We may do some experimentation by ourselves to find the best solution for us.
# Roller Styles

TL;DR: The ideal intake setup for 4476 seems to be hollow tubing rollers that rotate around a full width 3/8" round tube or hex shaft, whenever the intake doesn't require squishy wheels/mecanum wheels.

Currently in FRC, there are 3 prominent ways of designing an intake roller: live axle, full width dead axle, and separate dead axle. 
## Live Axle

The term "Live Axle" describes a setup where rotating objects (wheels, arms etc) are fixed on a shaft such that they rotate together. Bearings sit inside the side plates, the hex shaft with wheels on them rotate in the bearings. Extra standoffs are needed

![](https://i.imgur.com/sN3es2A.png)

Live axle intakes are quite common because they're relatively easy to make, and most hardware available have 1/2" hex bores built into them so it's very easy to slide them onto a hex shaft and call it a day. Live axles also allow for flexibility in plate placement, the side plates don't need to be on the outside of the axle.

To deconstruct a live axle roller, you'll need to unscrew the retention screws at the end of the axle, then slide the shaft out of the bearings. This process can be complicated by intermediate plates or wheels that are hard to shift around the shaft.
## Full Width Dead Axle

The term "Dead Axle" describes a setup where objects rotate around a stationary axle. The axle is connected connected rigidly to the side plate, and bearings sit inside wheels/rollers which spin around the stationary axle.

![](https://i.imgur.com/2kms0Id.png)
![](https://i.imgur.com/PC4xvNn.png)

Team [4414](https://www.chiefdelphi.com/t/team-4414-hightide-2023-robot-tsunami/428584/222?u=bdon) has made intakes this way for a few years, they do it with a [3/8" hex shaft](https://revrobotics.ca/rev-21-2076/) (red) spanning the width of the intake. They have a [1.25" polycarbonate roller](https://wcproducts.com/products/versarollers) with end plugs super glued into each end, which each have an integrated pulley and a space for the bearing to sit in. This design is very easy to replicate, and we can even think about using a [3/8" round shaft](https://wcproducts.com/products/shaft-stock) instead which would be usable with generic 0.375" ID bearings.

If a roller needs to be replaced, simply unscrew the bolts on each side and lift the roller assembly out. The shaft and bearings can be removed and reused if needed.
## Screw Dead Axle

This is another variation of the dead axle intake where instead of having a shaft go across the full width of the intake, you just have screws that hold a bearing on each end to the side plate. Additional standoffs are used if rigidity is needed. This style was used by [254](https://www.chiefdelphi.com/t/how-do-these-254-mechanisms-work-bearing-retention/409093/9?u=bdon) the last two years, and teams like [1678](https://www.chiefdelphi.com/t/1678-citrus-circuits-2023-cad-and-code-release/437632/30?u=bdon) are starting to adopt this style as it's completely optimized to save weight.

![](https://i.imgur.com/qtSv3nO.png)![](https://i.imgur.com/AyLOLMW.png)

The roller and end plug design stays very similar, the only change here is both teams mentioned above use bolts to connect their tube to their plugs instead of an adhesive. The end plugs have 2 bearings each to support loads better, and 254 adds a small modified piece of rounded hex for a better fit between the screw and the bearing.

To assemble this roller, the first step is to use a nut and bolt to secure each end plug to the side plates. Then the roller is slid into place and fastened using bolts. These steps are necessary because you need to hold onto the inner nut while screwing the bolt in from the side plate, but that nut is inaccessible when the roller is in place. The side plates therefore need some level of flex so that the roller is able to fit between the two end plugs after they are in place on the side plates.
## Conclusions

I prefer dead axle rollers over live axles for their light weight, packaging, and ease of assembly. They're lighter than live axle rollers because each wheel of a live axle is added weight on top of a beefier axle*. Dead axle rollers can be as small as 1.25" in diameter, which can help with packaging deployable intakes within a robot when retracted. Full width intakes are also the easiest of the bunch to assemble, as  However, designers need to be mindful of the mounting limitations of the dead axle roller, as well as the fact that [compliant wheels](https://www.andymark.com/products/4-in-compliant-wheels-options?via=Z2lkOi8vYW5keW1hcmsvV29ya2FyZWE6OkNhdGFsb2c6OkNhdGVnb3J5LzVhZjhlMjgzYmM2ZjZkNWUzNmYyMzk2YQ) and [mecanum wheels](https://wcproducts.com/products/mecanum-wheels) cannot be used with dead axle rollers**.

Between the two types of dead axle intakes, the full width axle is more approachable. It's more intuitive to assemble and disassemble, and comes with the benefit of not needing additional standoffs between the two plates which helps with packaging and ease of CAD. There may be a bit of a weight penalty, but since the screw dead axle setup requires a lot more hardware and double the amount of bearings, there shouldn't be a huge deficit.

\* A 23" wide intake with 2" flex wheels 2" apart on a 1/2" rounded hex axle weighs ~0.85 pounds, while a 1.25" diameter, 1/16" wall polycarbonate roller on a 3/8" rounded hex axle weighs ~0.46 pounds. Apologies for the amount of numbers, take a few read throughs lol.

** Technically, WCP sells 3", 4" and 5" compliant wheels with 1.1" round bores that can be stretched onto 1 1/8" or maybe even 1 1/4" rollers, but then a lot of the weight advantage from not having wheels is lost.

\- Brandon