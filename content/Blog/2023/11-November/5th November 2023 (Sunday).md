---
tags:
  - blog
date: 2023-11-05
---
# STEMLey Cup

We just finished competing in the STEMley Cup yesterday! Lots of good things to review, and we placed third captaining the 7th alliance captain.

## Scouting Review

The scouting system half functioned with our new website. 

Remember to bring power brick for [[scouting]] laptop

Allocate a phone for data to push stuff, check to see if it works on apple.

Communicate with scouts about event-strategy channel threads and can input on match planning

Look into sim card dongle data thing so we don't have to sacrifice a phone, team could get a cheap data plan

### What worked

- Tablet app worked well
- Server app scanning
	- csv generation
- [[Match]] Schedule
  The website just started working after match 14.
- Analysis page was decent

### What Broke
- Broke after match 28
- mass duplication of matches
### To Fix (tracked on [[Implement for 2024]])
- [ ] Check over /teams/XXXX for when db is accessed and why no data brakes the page
- [ ] Fix pushing that duplicates stuff
- [ ] When displaying numbers, round to sig figs
- [ ] Don't display "no comments" comments
- [ ] Some sort of search bar somewhere to select a team
- [ ] Link teams on analysis page to team page
- [ ] Make urls for specific views
- [ ] fix average game pieces, currently says no matches played
- [ ] have a way to update robot picture

## Pit Review

### What Went Well

### What Could Have Been Better

- There wasn't a lot for the third pit student to do, given that the the work and roles had been divided between the other two students for the season and they were accustomed to their tasks at that point.
	- Next season, we would want to have a third role and checklist defined
- Not specific to this event, but the bumpers took a harsh beating this year.
	- It may be worth trying iron on numbers next season - the numbers can be off to the left or right instead of centred on the long side of the robot so that it's more feasible to align them with our reversible bumper design.
# 2910 Engineering Process Talk

Their full talk can be found [here](https://www.youtube.com/watch?v=RhfuKh0JkVc)

## Takeaways

### Priority List
We can slightly modify our current [[Priority List]] process to make things clearer and ensure we have good design processes.

- Simplify our requirements process by making sub lists for each requirement.
	- Each subsystem should have requirements for
		- Speed
		- Orientation/Location
		- Consistency/reliability
	- There should also be overall robot requirements like:
		- COG
		- Holding things inside frame perimeter
- Remember that these goals can have timelines where the mechanism can evolve and get better over time.
  ![](https://i.imgur.com/cfR8AuH.jpg)

Make sure requirements are specific, measurable, attainable and relevant.

-Brennan

