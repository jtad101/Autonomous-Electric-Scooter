# Autonomous Navigation of an Electric Scooter
Open any one of the folders and run the `catkin_make` command in a terminal. Then source the `setup` file present in the `devel` folder to your terminal environment. 

## Map-based Autonomous Navigation
## To create a map
In terminal 1 - launch the gazebo world - roslaunch mybot_gazebo mybot_world.launch

In terminal 2 - build the map - roslaunch mybot_navigation gmapping_demo.launch

In terminal 3 - launch rviz - roslaunch mybot_description mybot_rviz_gmapping.launch

In terminal 4 - launch teleop - roslaunch mybot_navigation mybot_teleop.launch

## To save the map
In terminal 5 - save the map to a path - rosrun map_server map_saver -f ~/mybot_ws/src/mybot_navigation/maps/test_map

After saving the map close all windows and terminals.

## To load the map
In terminal 1 - launch gazebo - roslaunch mybot_gazebo mybot_world.launch

In terminal 2 - launch built map - roslaunch mybot_navigation amcl_demo.launch

In terminal 3 - launch rviz - roslaunch mybot_description mybot_rviz_amcl.launch

## Mapless Autonomous Navigation
### EKF
To launch the UKF Localized Autonomous Navigation run the command `roslaunch glide_2dnav outdoor_waypoint_nav.launch`
### UKF
To launch the EKF Localized Autonomous Navigation run the command `roslaunch glide_2dnav outdoor_waypoint_nav_ukf.launch`
