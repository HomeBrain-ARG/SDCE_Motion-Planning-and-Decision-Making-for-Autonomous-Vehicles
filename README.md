# **Udacity Self Driving Car Engineer Course**

## **Project Nº 5: SDCE_Motion-Planning-and-Decision-Making-for-Autonomous-Vehicles**

### [Go To Source Code Directly!!!]()

## **Project Overview:** <br />

In this project, you will implement two of the main components of a traditional hierarchical planner: The Behavior Planner and the Motion Planner. Both will work in unison to be able to:<br />

- Avoid static objects (cars, bicycles and trucks) parked on the side of the road (but still invading the lane). The vehicle must avoid crashing with these vehicles by executing either a “nudge” or a “lane change” maneuver.<br />
- Handle any type of intersection (3-way, 4-way intersections and roundabouts) by STOPPING in all of them (by default).<br />
- Track the centerline on the traveling lane.<br />

## **To accomplish this, you will implement:** <br />

- Behavioral planning logic using Finite State Machines - FSM.<br />
- Static objects collision checking.<br />
- Path and trajectory generation using cubic spirals.<br />
- Best trajectory selection though a cost function evaluation. This cost function will mainly perform a collision check and a proximity check to bring cost higher as we get closer or collide with objects but maintaining a bias to stay closer to the lane center line.<br />

