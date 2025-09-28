# STEPS BY STEPS

## 1. Using template, create a new name for robot

- create workspace from repo template into a file in laptop
- always source: $ source install/setup.bash
(Because sourcing only applies to the current terminal session. When you open a new terminal, it starts “fresh” and doesn’t remember your ROS2 environment variables.)
- launch bot from workspace: $ ros2 launch <robot_name> rsp.launch.py = $ ros2 launch articubout_one rsp.launch.py
  
## 2. Create a urdf for our robot and implement into rviz
## 3. Gazebo.

- go into workspace: $ cd dev_ws/
- source it: $ source install/setup.bash
- launch bot (with sim time enabled): $ ros2 launch articubot_one rsp.launch.py use_sim_time:=true
- launch gazebo: $ ros2 launch gazebo_ros gazebo.launch.py
- launch custom robot: $ ros2 run gazebo_ros spawn_entity.py -topic robot_description -entity bot_name
- wrap all of the commands into one single launch file in the workspace
- refresh with $ colcon build --symlink-install
- launch back that one command into the main command that has been sourced: $ ros2 launch articubot_one launch_sim.launch.py
- 
