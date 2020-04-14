UDACITY Project 2: Where am I?

1. Project Overview
This is the Where Am I? localization project of the Robotics Software Engineer Nanodegree program offered by Udacity. In this project, we utilize ROS AMCL package to accurately localize a mobile robot inside a map in the Gazebo simulation environments.

2. Description
The project is organized in the following directories:
```                                                      
                                              ├── where_am_I
                                              |   ├── src
                                              |   |   ├── my_robot
                                              |   |   |   ├── config
                                              |   |   │   │   ├── base_local_planner_params.yaml
                                              |   |   │   │   ├── costmap_common_params.yaml
                                              |   |   │   │   ├── global_costmap_params.yaml
                                              |   |   │   │   ├── local_costmap_params.yaml
                                              |   |   │   │   └── __MACOSX
                                              |   |   │   ├── launch
                                              |   |   |   |   ├── amcl.launch
                                              |   |   │   │   ├── robot_description.launch
                                              |   |   │   │   └── world.launch
                                              |   |   │   ├── maps
                                              |   |   │   │   ├── map.pgm
                                              |   |   │   │   └── map.yaml
                                              |   |   │   ├── meshes
                                              |   |   │   │   └── hokuyo.dae
                                              |   |   │   ├── urdf
                                              |   |   │   │   ├── my_robot.gazebo
                                              |   |   │   │   └── my_robot.xacro
                                              |   |   |   ├── world
                                              |   |   │   |   └── georgios.world
                                              |   |   │   ├── CMakeLists.txt
                                              |   |   |   └── package.xml
                                              |   |   ├── CMakeLists.txt
                                              |   |   └── where_am_I.rviz
                                              |   └── 
                                              └── README.md 
   

  ```
