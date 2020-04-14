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

3. How to build the project

  - Clone this repository into the workspace.
  - Build the project using the following commands:
  ```
  $ cd /home/workspace/
  $ catkin_make
  $ source devel/setup.bash
  ```
  - Execute the project using the following commands:
  ```
  $ roslaunch my_robot world.launch 
  $ roslaunch myamcl amcl.launch
  ```
  - For RVIZ Integration: 

   `Select: Global Options-> Fixed Frame-> Map`

   `Add Robot Model.`
   
   `Add Camera. Then Select Image Topic: /camera/rgb/image_raw.`
   
   `Add LaserScan. Then Select Image Topic: /scan.`
   
   `Add Maps. Then Select Image Topic: /map. Check other maps such as /move_base/local_costmap/costmap /move_base/global_costmap/costmap`
   
   `Add PoseArrow. Then Select Topic: /pointcloud.`

  - Additionally, move commands can be sent to robot through the teleop package. To start teleop, run the following command in the terminal: ` teleop_twist_keyboard teleop_twist_keyboard.py `
