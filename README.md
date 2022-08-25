# Mobile Robots and Path Planning

This is an introductory set of packages in ROS noetic to display different
types of motion in robots and basic path planning algorithms.
These are packages taken from multiple sources which I have updated in some
cases ways to explore their control.

## Package Overview

There are 4 packages to be explored in this repo, namely

 - [Skidsteer Drive](./skidsteer_drive) Created by [Macavitycode](https://github.com/Macavitycode)
 - [Ackermann Drive](./ackermann_drive) Created by [aizzat](https://github.com/aizzat) ([original package](https://github.com/aizzat/ackermann_vehicle), with reference from [trainman419](https://github.com/trainman419) and [hdh7485](https://github.com/hdh7485))
 - [Omniwheel Drive](./omniwheel_drive) Created by [arthurgomes4](https://github.com/arthurgomes4) ([original package](https://github.com/arthurgomes4/omni_wheels_simulation))
 - [Simple Drone](./simple_drone) Created by [NishanthARao](https://github.com/NishanthARao) ([original package](https://github.com/NishanthARao/ROS-Quadcopter-Simulation/tree/master/urdf))

Skidsteer is a very easy configuration and can be an entry point of sorts to
the control schemes.
It uses a readily available Gazebo plugin for control.

Ackermann and Omniwheel are a little more complex and have custom/special
control scripts attached, as seen in the package.

The drone simulation is also using a custom controller script.

## Usage

There are slightly different commands and steps to run the simulations for all
the mentioned mechanisms.

### Prerequisites

For these packages to work, ensure you have the following list of packages
installed and setup:

```bash
ros-noetic-xacro ros-noetic-robot-state-publisher
ros-noetic-teleop-twist-keyboard ros-noetic-rviz
ros-noetic-velocity-controllers ros-noetic-effort-controllers
ros-noetic-position-controllers ros-noetic-controller-*
ros-noetic-joint-state-* ros-noetic-controller-manager* 
ros-noetic-joint-state*
```

Clone this repository into `(your_catkin_workspace)/src`, source the
ennvironment and run `catkin_makke`.
All these packages can be controlled using the teleop twist keyboard as
provided by ROS.
Each package's usage is explained below.

### Skidsteer Drive

The package can be run by using

```bash
roslaunch skidsteer_drive bot.launch
```

