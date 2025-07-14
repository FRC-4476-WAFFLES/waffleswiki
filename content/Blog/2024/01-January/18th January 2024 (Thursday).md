---
tags:
  - blog
date: 2024-01-18
---
Day 13

# Shooter Prototyping

We finally have finished our primary shooting prototype. Best compression we found was 5.5", and our main focus for the last two days has been testing accuracy for two wheels on shooter vs one.

INSERT TONS OF SHOOTING VIDEOS

Our main takeaways is that for the most part the accuracy doesn't change much, seems like compression and shooter rigidity covers most of that, but what does change is the amount that the note is accelerated. Our range when testing was good for the two wheel variant, and while we didn't explicitly test range with single wheel, from the videos we can see the exit velocity of the note is much higher with two wheels on either side. As a result of this testing we are sticking to the two wheel per side model, even though it takes up more space.

## Speed up Time

There was also a lot of discussion about the amount of time that the shooter would need to spin up to the correct RPM for a shot. By our current estimations a shooter with kraken should take a bit under a second to spin up to speed for a close shot, and about 2 seconds for a long shot. So far this seems adequate.

Here is some calculations with what we expect.

![](https://i.imgur.com/wvA7En4.png)

# Design Review

We had our third design review, this time with previous mentor Michael N.

## Notes from review

- Intake support/front of chassis
- Which weighs more, steel plate or aluminum plate + tubing?  Do we want it to weigh more or less?  COG considerations
- Could add angled crossmembers across the corners
- Add flanges to aluminum shooter plate to add rigidity
- Could run structural ribs along the underside for more rigidity if needed
- Could add funneling to shooter if needed
- Could test interfacing between existing intake and theoretical shooter for vertical/angular directions
- Deploying kicker - look at 610’s 2016 robot for potential inspiration
- Could maybe not extend full elevator until climb, that could trigger deploy potentially
- Constant force springs
- Could use carabiners for stationary climber hooks
- Look into Ansys Discovery (free) software for FEA on front crossmember

# Shooter CAD

Top geometry and general layout has been done, we probably will need to do some rejigging for how we will mount this to a pivot for the shooter, but for now it's okay.

![](https://i.imgur.com/SoUpacY.png)

# Intake CAD

![](https://i.imgur.com/eoNCTMk.png)

Things are slowly coming together, getting rollers on as well as front cross member.

# Drive Train

![](https://i.imgur.com/BXr244r.png)
Added a couple mounting holes for the swerves.

# Elevator

![](https://i.imgur.com/U8M4lez.png)

Bearings and gussets got revamped/added. There are some concerns of actually running the wires for the elevator up the tube of the first stage. This is something we will have to work through tomorrow and over the weekend.

-Brennan

