
# Research_Track_1-final-assignmnet (Ginne vikas Reddy) (matricola 5061211)

## Overview of the project

  This project was developed to simulate the robot by using navigation stack in a 3D environment, In this project the robot is supposed to simulate 4 tasks entered by the user.

## General information regarding the project

   In this project the robot is localized by user input, these are the following steps that robot can perform these tasks

   1.Move randomly in the environment, by choosing 1 out of 6 possible target positions (-4,-3) (-4,2) (-4,7) (5,-7) (5,-3) (5,1).

   2.Ask the user to enter next target position from the random six.

   3.To start followng the external walls given in the map.

   4.To enter standby position.

## How robot is controlled in these conditions

 #### Random target
  When input is 1 from the user, A random goal is generated from random_goal_generator which will publish to move_base/goal topic and robot wil start moving to that location

#### Selected target
if the user enters 2 as the input, the user_interface will ask to pick a target from a list of possible destinations. Wall follower:

#### Wall follower
if the user enters 3 as the input, the robot will follow the walls by calling wall_follower_switch service through a servie client which allows robot to follow external walls.

#### Standby
in case of pressing 4,the velocities are set to 0 ,then the robot will stop for certain amount of time .

## List of nodes used
![Screenshot 2021-04-17 at 3 10 04 PM](https://user-images.githubusercontent.com/73032093/115137406-3b5bb780-a026-11eb-9b82-f1f826591eef.png)

## list of topics used 
![Screenshot 2021-04-17 at 3 10 58 PM](https://user-images.githubusercontent.com/73032093/115137454-7d84f900-a026-11eb-8259-6d61ea7505e7.png)

## software Architecture
![rosgraph](https://user-images.githubusercontent.com/73032093/115157775-97e8c200-a07a-11eb-945b-17eff98c5c36.png)

## How to run the code

git clone the package

`https://github.com/vikasreddy636/Research_Track_1-final-assignmnet.git`

create a workspace in root repositories

`mkdir "name of the workspace" `

move the git package to the src folder of that workspace

Build the package

`catkin_make`

Refresh the workspace using

`rospack profile`

in the folder "Research_Track_1-final-assignmnet/final_assignment/scripts/" check for read and write permissions

`ls -la`

to give permissions to individual file

`chmod +x <file name.py>`

In the terminal excute the following commands 

TO  launch Gazebo and Rviz using launch commands

`roslaunch final_assignment simulation_gmapping.launch`

`roslaunch final_assignment move_base.launch`

for wall follow service

`rosrun final_assignment wall_follow_service_m.py`

To start the server

`rosrun my_srv Final_project_server`

To excute the final program

`rosrun final_assignment Final_code.py`

For Computational graph

`rqt_graph`

## Errors that might occur in noetic

missing of move_base file

To fix that error 

`cd /opt/ros/noetic/lib `

`sudo apt-get install ros-noetic-move-base-msgs`










