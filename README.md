UDACITY Project 3: Map my world

1. Project Overview

This is the Map My Worls project of the Robotics Software Engineer Nanodegree program offered by Udacity. In this project, we will create a 2D occupancy grid and 3D octomap from a simulated environment using the robot from the 2nd Project of the program  with the RTAB-Map package. 

The second project stated here and on which this project is based, is the "where am I?"
(https://github.com/geo196/where_am_I.git)


2. Description

The project is organized in the following directories:
```                                                      
── where_am_I
   ├── src
   |    my_robot
   |   |   ├── config
   |   │   │   ├── base_local_planner_params.yaml
   |   │   │   ├── costmap_common_params.yaml
   |   │   │   ├── global_costmap_params.yaml
   |   │   │   ├── local_costmap_params.yaml
   |   │   │   └── __MACOSX
   |   │   ├── launch
   |   |   |   ├── amcl.launch
   |   |   |   ├── localization.launch
   |   |   |   ├── mapping.launch
   |   │   │   ├── robot_description.launch
   |   │   │   └── world.launch
   |   │   ├── maps
   |   │   │   ├── map.pgm
   |   │   │   └── map.yaml
   |   │   ├── meshes
   |   │   │   └── hokuyo.dae
   |   │   ├── urdf
   |   │   │   ├── my_robot.gazebo
   |   │   │   └── my_robot.xacro
   |   |   ├── world
   |   │   |   └── georgios.world
   |   │   ├── CMakeLists.txt
   |   |   └── package.xml
   |   ├── teleop_twist_keyboard
   │   |   ├── CHANGELOG.rst
   │   |   ├── CMakeLists.txt
   │   |   ├── README.md
   │   |   ├── package.xml
   |   |   └── teleop_twist_keyboard.py
   |   ├── CMakeLists.txt
   |   └── where_am_I.rviz
   └── README.md 
```


3. How to build the project

  - Clone this repository into the workspace.
  - Build the project using the following commands:
  ```
  $ cd /home/workspace/
  $ catkin_make
  $ source devel/setup.bash
  ```
  - Execute the project using the following commands in different terminals:
  ```
  $ roslaunch my_robot world.launch 
  $ roslaunch my_robot localization.launch
  $ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
  ```
  The teleop package is used to send move commands to the robot
  - For the RVIZ is used the same configuration with the 2nd project: 
      where_am_I.rviz
  - A database viewer is also used for the database analysis. In a new terminal:
  ```rtabmap-databaseViewer ~/.ros/rtabmap.db```
  ```
  in popup window: use the database parameters: yes.
  View -> Constraint View.
  View -> Graph View.
  ```

