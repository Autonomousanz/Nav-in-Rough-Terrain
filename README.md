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
2. Launching the robot in this environment using the launch file in the catkin workspace which contains the world file location
3. Generate a pgm file through slam mapping of this environment, the pgm file is already available by default in the husky clearpath installation.
4. 

## Results :

[![Runtime](https://github.com/Autonomousanz/Autonomous-Navigation-in-Rough-Terrain/blob/master/Videos/run.gif)

## Conclusion :


## Future Work :






