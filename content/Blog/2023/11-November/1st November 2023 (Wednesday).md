---
tags:
  - blog
date: 2023-11-01
---
# Igus Chain 254

> [!quote] Pat Fairbank
> From our records, it looks like the part we used this year was E045-10-018-0. We order directly from igus using their website.

For future reference when we want to get igus chain. I know the stuff we used for [[2019 Robot Charlie]] was pretty flimsy and could be a lot better.

# Swerve Ratios

[[West Coast Products]] has released a video of them putting their new [[Kraken X60|Kraken X60]] motor head to head against the [[Falcon 500]]. However, they changed the gear ratio from 6.53 : 1 on their Falcon robot to 5.14 : 1 on their Kraken robot, which is a much more aggressive gear ratio which would decrease torque and increase speed at the wheels. This would cause a 

Since we're interested in using Krakens on our swerve drive, we should consider swapping out the gear ratio of our swerve modules.

The [ILITE Drivetrain Simulator](https://www.chiefdelphi.com/t/ilite-drivetrain-simulator-v2020/369188) was used to simulate the performance of different motor and ratio combinations, with wheel diameter set to 4 inches, robot inspection weight and auxiliary weight to 120 and 27 pounds respectively, and rest battery voltage at 12.4V. The Kraken motor is not officially in the simulator, so a new motor was added with the FOC specs from [WCP's documentation](https://docs.wcproducts.com/kraken-x60/overview-and-features/motor-performance).

![](https://i.imgur.com/s39XeT0.png)

The L1 Falcon was the configuration run on [[2023 Robot Misha and Zoey]] and will be used as a baseline to compare the rest of the results to. The L1 Kraken would be a straight motor upgrade, the L2 Kraken and L3 Kraken configuration

Results are as follows:

|  | 10ft Time (s) | 20ft Time (s) | 40ft Time (s) | Free Speed (ft/s) | Min Voltage (V) |
|---|---|---|---|---|---|
| L1 Falcon | 1.12 | 1.96 | 3.60 | 12.1 | 8.923 |
| L1 Kraken | 1.16 | 2.08 | 3.88 | 11.0 | 9.093 |
| L2 Kraken | 1.08 | 1.84 | 3.32 | 13.3 | 8.430 |
| L3 Kraken | 1.04 | 1.72 | 3.12 | 14.6 | 8.215 |

Based on these numbers, the L2 Kraken looks like the most well balanced between having good performance while keeping the battery at an safe voltage to prevent brownouts. However, a final decision will be made after kickoff so we can get make a more educated decision on which ratio would suit the game best. When it comes time to change our swerve ratios, we will have to buy a replacement [double gear](https://www.swervedrivespecialties.com/collections/mk4i-parts/products/27t-50t-20dp-double-gear?variant=39377997987953) and a matching [single gear](https://www.swervedrivespecialties.com/collections/mk4i-parts/products/27t-50t-20dp-double-gear?variant=39377997987953).

\- Brandon