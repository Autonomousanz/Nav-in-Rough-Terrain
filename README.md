# Autonomous-Navigation-in-Rough-Terrain


This is project inspired from the Mathworks Matlab - Excellence in Innovation Repository :
https://github.com/mathworks/MathWorks-Excellence-in-Innovation.git
The details of the project is illustrated on the project 209 readme with A* Path planning and obstacle avoidance in a warehouse example.

## Motivation :
Autonomous navigation on off-road environment such as agricultural lands is significant in the development of autonomous vehicles.  Off-road terrain brings alot of complex problems such as uneven-ground with uncertain paths for an autonomous vehicle to traverse. In order to overcome these limitations a robust path planning algorithms and dynamic obstacle avoidance model must be deployed on the vehicles. Navigating complex terrain at speed and with minimal human supervision is a major challenge for developing such systems.


## Description :

The project is an experiment of finding the shortest path to a given set of start and end points namely waypoints using RRT* Path planning algorithm in a rough terrain and then deploying these waypoints on the turtlebot robot. Mainly the tools used were MATLAB for generating the waypoints using a map of the given environment in pgm file, further more feeding this shortest path to a robot in Gazebo Ros simulation using the simulink model.

## Procedure :
Following are the steps taken for running this project -
1. Below is a rough terrain environment suitable for the application - source: husky clearpath , husky playpen environment :
[!environment](https://github.com/Autonomousanz/Autonomous-Navigation-in-Rough-Terrain/blob/master/Pictures/huskeyplaypath.png)

2. Launching the robot in this environment using the launch file which contains the world file location in the catkin workspace 
3. Generate a pgm file through slam mapping of this environment, the pgm file of the chosen environment is already available by default in the husky clearpath installation.

![map pgm file](https://github.com/Autonomousanz/Autonomous-Navigation-in-Rough-Terrain/blob/master/Pictures/map.pgm)

4. Once the pgm file is available, use a matlab mlx script RRT planner to generate a path using RRT* algorithm. One major challenge is to transform the coordinates of gazebo world with the exact coordinates from pgm file format.

![RRT planner path generated](https://github.com/Autonomousanz/Autonomous-Navigation-in-Rough-Terrain/blob/master/Pictures/Picture1.jpg)

5. A roslocation.cpp script was used to establish a correlation with map coordinates on the pgm file and the gazebo simulated environment
6. After creating the waypoints, the last point is goal of the trajectory which needs to be transformed back into gazebo coordinates. The mathworks path following with obstacle avoidance slx file takes this goal point as input to then generate the corresponding velocity upon connection with gazebo simulation. a rosinit command must be initialized in the command line of matlab to establish ros master connection with the turtlebot.
7. The robot then traverses the given path and goal set in Gazebo environment after the simulink model runs successfully.

## Results :

![Runtime](https://github.com/Autonomousanz/Autonomous-Navigation-in-Rough-Terrain/blob/master/Videos/run.gif)

## Conclusion :
Autonomous Navigation using RRT* path planning algorithm  

## Future Work :






