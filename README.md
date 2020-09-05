# barrett_hand
Configuration of the Robotnik Automation ROS package for the barrett hand (tested with BH8-280 model)

## Dependencies
### pcan-python
- swig
- gcc
- python 2.7
- pcan driver version >= 8.6 (visit https://www.peak-system.com/Details.114+M52b3b89ad2b.0.html?&L=1)

Use make to build and install pcan driver:

    tar –xzf peak-linux-driver-X.Y.Z.tar.gz
    cd peak-linux-driver-X.Y.Z
    make clean
    make NET=NO_NETDEV_SUPPORT
    sudo make install

---
**Important**

pcan driver only works with the version of the Linux kernel (LTS Ubuntu kernel is recommended) that the machine was running during compilation. If the kernel is updated, the driver must be recompiled.

---

## Instalation (ROS Kinetic on Ubuntu 16.04.6 LTS)

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

