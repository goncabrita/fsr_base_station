##Installation

###Step 1. Install ROS
Follow the instructions on http://wiki.ros.org/hydro/Installation/Ubuntu to install ROS Hydro on your Ubuntu.

###Step 2. Install wstool
Open a terminal window and install wstool using apt-get:
$ sudo apt-get install python-wstool

###Step 3. Install the FSR Base Station software on its workspace
Open a terminal window and run the following commands:
$ source /opt/ros/hydro/setup.bash
$ mkdir ~/fsr_base_station_workspace
$ cd ~/fsr_base_station_workspace
$ wstool init src  -j8
$ rosdep install --from-paths src -i -y
$ catkin_make
$ source ~/fsr_base_station_workspace/devel/setup.bash

Finally add the source command to your .bashrc file for commodity:
$ echo source ~/fsr_base_station_workspace/devel/setup.bash >> ~/.bashrc

