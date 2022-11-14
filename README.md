# **Udacity Self Driving Car Engineer Course**

## **Project Nº 5: SDCE_Motion-Planning-and-Decision-Making-for-Autonomous-Vehicles**

### [Go To Source Code Directly!!!]()

## **1) Project Overview:** <br />

In this project, you will implement two of the main components of a traditional hierarchical planner: The Behavior Planner and the Motion Planner. Both will work in unison to be able to:<br />

- Avoid static objects (cars, bicycles and trucks) parked on the side of the road (but still invading the lane). The vehicle must avoid crashing with these vehicles by executing either a “nudge” or a “lane change” maneuver.<br />
- Handle any type of intersection (3-way, 4-way intersections and roundabouts) by STOPPING in all of them (by default).<br />
- Track the centerline on the traveling lane.<br />

## **2) To accomplish this, you will implement:** <br />

- Behavioral planning logic using Finite State Machines - FSM.<br />
- Static objects collision checking.<br />
- Path and trajectory generation using cubic spirals.<br />
- Best trajectory selection though a cost function evaluation. This cost function will mainly perform a collision check and a proximity check to bring cost higher as we get closer or collide with objects but maintaining a bias to stay closer to the lane center line.<br />

## **3) Modify the following files:** <br />
- behavior_planner_FSM.cpp<br />
- cost_functions.cpp<br />
- motion_planner.cpp<br />
- velocity_profile_generator.cpp<br />

## **4) Project Setup Instructions:** <br />

Follow the series of the commands in the workspace to launch the CARLA simulator:<br />

### **New terminal window:**<br />
```
1. su - student
// Will say permission denied, ignore and continue 
2. cd /opt/carla-simulator/
3. SDL_VIDEODRIVER=offscreen ./CarlaUE4.sh -opengl
```

### **New terminal window:** <br />
```
4. git clone https://github.com/udacity/nd013-c5-planning-starter.git
5. cd nd013-c5-planning-starter/project
6. ./install-ubuntu.sh
7. cd starter_files/
8. cmake .
9. make
10. cd nd013-c5-planning-starter/project
11. ./run_main.sh
// This will silently fail 
12. ctrl + C to stop 
13. ./run_main.sh again
14. Go to desktop mode to see CARLA

// If error bind is already in use, or address already being used
ps -aux | grep carla
kill id
```
<br />

## **5) Results:** <br />
Parameters selected: P_NUM_PATHS = 10 and P_NUM_POINTS_IN_SPIRAL = 20 <br />

