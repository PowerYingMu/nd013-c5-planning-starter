# Motion Planning and Decision Making

## Introduction

In this project, two of the main components of a traditional hierarchical planner are implemented, which are the Behavior Planner and the Motion Planner. Both will work in unison to be able to:
1. Avoid static objects (cars, bicycles and trucks) parked on the side of the road (but still invading the lane). The vehicle must avoid crashing with these vehicles by executing either a “nudge” or a “lane change” maneuver.
2. Handle any type of intersection (3-way, 4-way intersections and roundabouts) by STOPPING in all of them (by default)
3. Track the centerline on the traveling lane.

To accomplish this, the following items are implemented:
1. Behavioral planning logic using Finite State Machines - FSM
2. Static objects collision checking.
3. Path and trajectory generation using cubic spirals
4. Best trajectory selection though a cost function evaluation. This cost function will mainly perform a collision check and a proximity check to bring cost higher as we get closer or collide with objects but maintaining a bias to stay closer to the lane center line.

## Results

The following figiure shows taht the ego vehicle can avoid a parked car on the roadside. The ego car changes the lane and follow the lane cebter by behavioral planning.

![image](/project/Results/EgoPassParkedCar.png)
