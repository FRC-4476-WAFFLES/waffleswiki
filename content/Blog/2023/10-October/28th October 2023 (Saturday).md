---
tags:
  - blog
  - CAD
  - elevator
  - buildseason
date: 2023-10-28
---
# 254 Elevator Kickstand

> [!quote] [Torrance on Chief Delphi](https://www.chiefdelphi.com/t/team-254-presents-2023-breakdown-technical-binder-code-q-a/443167/39?u=brennanb)
> A nifty little kickstand exists to let the carriage start the match 2/3rd of the way up, for fast initial object placement. A 3D printed piece pivots on a shoulder bolt and is tensioned away from the elevator with some rubber bands. It can pushed against the upright tube as the [[Elevator|elevator]] carriage bearing is lowered onto it. When the auton starts, the carriage goes up and the rubber bands pull the kickstand out of the way for the rest of the [[Match]] to allow all motion.

Seems like a neat way to have the [[Elevator|elevator]] carriage start at an alternate starting position that isn't the ground if needed. Nice and simple to execute.

![](https://i.imgur.com/MW8skOh.png)
![](https://i.imgur.com/GRsihbq.png)

-Brennan

Only a week until STEMley! Very exciting, last full day of [[Drive Practice]] today at the [[Kingston Robotics Lab]] to get our [[Driver]] and [[Operator]] synergy up.

> [!quote] [Brennan from Thursday](https://wiki.wafflesrobotics.com/Blog/2023/10-October/26th-October-2023-(Thursday))
> 
> Wiring hall effect sensors directly to a falcon wasn't something I was even aware of. This seems like a nice way to do it, and I assume the kraken is also capable of doing this, but we should check!

Today as the bearer of bad news updating the blog from two days back, the [[Kraken X60|kraken]] appears uncapable of doing this. Sadness. I'll upload a picture explaining why later today when I can figure out how the imgur plugin works.

edit: this doesn't exist on the kraken
![](https://i.imgur.com/lCMQ3gg.png)
-Taegen

# Technical Leads Meeting

### New Workspace at [[Kingston Robotics Lab]]!
Things we want to use it for:
- practicing
- tuning autos
- using the big tools (has to be done with an 'expert [[mentor]]' for supervision, which we should decide who those will be in advance of build season to get them properly trained)
- using the 3d printers
- using the computers on an as-need basis
- using the "classroom" space to program or have other students working on things like [[awards]] handouts to break into smaller groups

### What is our scheduling plan? 

Where are we going to be, when?
- Early season at SH when formulating robot ideas/concepts

Where do we want to assemble robot?
- more space to do majority of it at SH, if we need to do some manufacturing we can bring over material and do it there
- this includes wiring
- should work on a better system for spray painting but still do at SH

When the robot is assembled?
- initial [[Software|programming]] can be done at SH
- move when the robot is testable and theoretically works
- maybe look at using the family day weekend as a milestone for the move to BGC - leave out of SH and return and move in to BGC?

What about when we can't meet at BGC? what do we do
- goal is to leave the robot there
- [[Meetings]] at SH
	- iterations/cad focus, [[manufacturing]], and award focus
- [[drive team]] takes days off ideally

are we still going to family day weekend?
- plan for it
- tell (force? threaten?) good teams to come to us and pray for the best

are we going to build field elements at SH?
- just enough to prototype until the robot is working
- things that are feasible and needed

### In-Season [[Meetings]]

in season meeting times:
At least one of us should be at a meeting, likely will end up 2 
Q has alternating labs on monday/tuesday nights
Brandon possibly unavailable weekend nights
Brennan has preference to weekends
generally makes sense for taegen/brennan to go in at same times
Eden and taegen avail TBD

Overall work load:
Eden/brandon are early on
quinton/taegen are during assembly/wiring/getting robot ready to go
Brennan is more of a mid-end of season dude

weeknights from 18:30-21:30
weekend possibly 10-7, with shifts from 10-3 and 2-7
when we can't do sunday mornings at BGC we can just run a BGC shift from 2-7 and the morning dudes can be at SH

still need to check in with students on times for build season and if they would show up pre-noon, but will try that

looking at maybe running friday long and doing a [[parent]] dinner that day, and have it BYO food on weekends (T and Q could cover most, starting at 3:30ish)

do we want CAD [[Meetings]] to be online focused? some people can only CAD at home - maybe hybrid?
- B +E more comfortable teaching people who are less familiar with [[Solidworks]] in person, but experienced designers/those who need to can stay home and work on personal PC
- brennan can join in
- move to [[Slack]] huddles for this purpose
- will do our best to push screensharing, anticipate some pushback but too bad

is there anything we want to store at BGC? there's shelves and stuff
- small amount of spare tools
- maybe just put all the stuff that would be stored in the [[Pit]] under tables there to make it a little bit more spread out
- could move some stuff that we don't need access to very regularly (robot graveyard?)
- some spare materials? scrap material like L brackets, some spare tubing
- use the space as spare space to work if needed

# Drive Practice

We had the aforementioned [[Drive Practice]] session! We had some good hours of running but some unfortunate [[Software|software]] issues had us stuck for the first two hours and 41 minutes.

We accidentally deployed an incomplete version of code to the robot as we had tried to update to Phoenix V6 a few weeks back and that took more work than we thought it would (so still on the todo list for 2024). The calibration for the arm was off as a result which was giving some really weird readout values - fixed that by going through constants.java and setting the shoulder left/right calibration variables to what was seen in [[WPILib]] [[Shuffleboard]].

At some point, one of the bolts mounting the intake gearbox came undone and the whole gearbox tilted down into the [[Polycarbonate|polycarb]] belts. Friction energy dissipates as heat so the [[Anderson PowerPole]]s on the motor needed to be replaced...

![](https://i.imgur.com/KkPZGsP.png)

Melting plastic aside, the practice seemed to go well. Sebi and Finlay are our [[Driver]] and [[Operator]] for STEMley, and Sylvan got in some good [[Human Player]] practice as well. Good luck to our 3/5ths new [[Drive Team]] at the event (new [[Technician]] too, go Kenneth!)!

-Taegen

# MK4I assembly with Krakens

As part of the cooling system built into the [[Kraken X60|kraken]], the cooling screw will have to be removed and covered with a piece of tape as per [this post](https://www.chiefdelphi.com/t/announcing-kraken-x60-powered-by-talon-fx/442236/413?u=tmpoles)

-taegen
