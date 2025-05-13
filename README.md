[中文](./README_CN.md)

# ELITE Robots ROS 2 tutorials
This package contains tutorials around the ROS 2 packages for Elite Robots.

## Getting started
To use the tutorials from this repository, please make sure to [install ROS2](https://docs.ros.org/en/humble/Installation.html) on your system. This repository is for ROS2 Humble only.

To use the tutorials from this repository, please make sure to [install Elite_Robots_CS_ROS2_Driver](https://github.com/Elite-Robots/Elite_Robots_CS_ROS2_Driver) on your system. This repository is for Elite_Robots_CS_ROS2 main branch now.

With that, please create a workspace, copy this folder into the workspace, install the dependencies above and build the workspace.

1. Create a colcon workspace:
   ```bash
   export COLCON_WS=~/workspaces/elite_tutorials
   mkdir -p $COLCON_WS/src
   ```

2. Copy the required repositories and install package dependencies:
   ```bash
   cd $COLCON_WS
   git clone https://github.com/Elite-Robots/Elite_Robots_CS_Ros2_Tutorials.git src/elite_tutorials
   rosdep update && rosdep install --ignore-src --from-paths src -y
   ```
   
3. Create a colcon workspace:
   ```bash
   cd $COLCON_WS
   colcon build
   ```

4. Source your workspace:
   ```bash
   source $COLCON_WS/install/setup.bash
   ```

5. Launch an example:
   e.g. the custom work cell example
   ```bash
   ros2 launch my_elite_robot_cell_control start_robot.launch.py use_fake_hardware:=true
   ```

6. You can use [Elite Robots ROS2 tutorials](./tutorials/Elite Robots ROS2 tutorials.md) to get more useful informations.
