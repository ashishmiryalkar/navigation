# navigation
Navigation of turtlebot3 robot using nav2 stack.

turtlebot3 with building model in gazebo
ros2 launch turtlebot3_gazebo turtlebot3_house.launch.py

to create map.
run rviz,
ros2 launch cartographer_slam cartographer.launch.py
add Map, TF, LaserScan in rviz.
manually move the robot inside the environment. using teleop_keyboard pkg and the cartographer will generate the map of the environment.
make sure to publish /scan - laser data, /odom - odometry data for the cartographer to work.

all settings for rviz are present in mapper_config.rviz
![Alt text](<Screenshot from 2023-10-25 13-44-12.png>)

Localization
ros2 launch localization localization.launch.py
do global position localization ros2 service call /reinitialize_global_localization std_srvs/srv/Empty

rotate the robot using teleop_twist keyboard to localize itself.