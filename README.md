# barrett_hand
Configuration of the Robotnik Automation ROS package for the barrett hand (tested with BH8-280 model)

## Instalation

Use make to build and install pcan-python (check dependencies):

    git clone https://github.com/RobotnikAutomation/pcan_python.git
    make
    sudo make install

Use catkin to build and install barrett_hand:

    cd ~/catkin_ws/src
    git clone https://github.com/RobotnikAutomation/barrett_hand/tree/kinetic-devel
    cd ..
    catkin build
    source devel/setup.bash

Add /usr/lib to the PYTHONPATH

    export PYTHONPATH=/usr/lib:$PYTHONPATH

