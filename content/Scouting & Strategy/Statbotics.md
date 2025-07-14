Statbotics uses the [[FIRST API]] to calculate statistics for [[FRC]] teams/matches. 

## Features
[[Match]] Predictions
Team Rankings
Event Predictions
EPA

## EPA (Expected Points Added)

Each team starts with an Elo rating of 1500. An alliance's rating is the sum of the ratings of its three teams. To predict the winner of a match, the Elo ratings of the two alliances are compared. The win probability is a logistic function of the difference between the two ratings, where d is the difference between the two ratings:

![](https://i.imgur.com/g7fcjU9.png)

After the match, the rating of each team on the winning alliance is increased, and the rating of each team on the losing alliance is decreased. The amount of change is proportional to the surprise of the outcome. Since each year is a new game, scoring must be standardized into consistent units. This is done by dividing by the standard deviation of Week 1 scores. The predicted score margin is defined as 0.004 times the difference in ratings, and the actual score margin is the difference between actual scores divided by the standard deviation. The amount of change is then proportional to the difference between the predicted and actual score margins:

![](https://i.imgur.com/BNTPGHd.png)

where K is a constant that controls the amount of change. K is set to 12 for qualification matches and 3 for playoff matches. Small adjustments are made to penalize rookie teams and apply mean reversion year over year.


[Statbotics](https://www.statbotics.io/)
