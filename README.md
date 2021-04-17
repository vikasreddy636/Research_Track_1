# Research_Track_1-final-assignmnet (Ginne vikas Reddy) (matricola 5061211)

## Overview of the project

  This project was developed to simulate the robot by using navigation stack in a 3D environment, In this project the robot is supposed to simulate 4 tasks entered by the user.

## General information regarding the project

   In this project the robot is localized by user input, these are the following steps that robot can perform these tasks

   Move randomly in the environment, by choosing 1 out of 6 possible target positions (-4,-3) (-4,2) (-4,7) (5,-7) (5,-3) (5,1).

   Ask the user to enter next target position from the random six.

   To start followng the external walls given in the map.

   To enter standby position.

 #### Random target
  When input is 1 from the user, A random goal is generated from random_goal_generator which will publish to move_base/goal topic and robot wil start moving to that location


if the user press  2, the user_interface will ask to pick a target from a list of possible destinations. Wall follower:
if the user press 3, the robot will follow the walls by calling wall_follower_switch service.
in case of pressing 4,the velocities are set to 0 ,then the robot will stop.
  
