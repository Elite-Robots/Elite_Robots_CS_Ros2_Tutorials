[English](./README.md)

# ELITE Robots ROS 2 教程
这个软件包包含了围绕 Elite Robots 的 ROS 2 软件包的相关教程。

## 开始使用
要使用此仓库中的教程，请确保在您的系统上 [安装 ROS2](https://docs.ros.org/en/humble/Installation.html) 。 此仓库仅适用于 ROS2 Humble 版本。

要使用此仓库中的教程，请确保在您的系统上 [安装 Elite_Robots_CS_ROS2_Driver](https://github.com/Elite-Robots/Elite_Robots_CS_ROS2_Driver)。目前，此仓库适用于 Elite_Robots_CS_ROS2 的主分支。

在此基础上，请创建一个工作空间，将此文件夹复制到工作空间中，安装上面的依赖项，然后构建工作空间。

1. 创建一个 colcon 工作空间:
   ```bash
   export COLCON_WS=~/workspaces/elite_tutorials
   mkdir -p $COLCON_WS/src
   ```

2. 复制所需的仓库并安装软件包依赖项:
   ```bash
   cd $COLCON_WS
   git clone https://github.com/Elite-Robots/Elite_Robots_CS_Ros2_Tutorials.git src/elite_tutorials
   rosdep update && rosdep install --ignore-src --from-paths src -y
   ```
   
3. 创建一个 colcon 工作空间:
   ```bash
   cd $COLCON_WS
   colcon build
   ```

4. 加载你的工作空间:
   ```bash
   source $COLCON_WS/install/setup.bash
   ```

5. 运行一个示例:
   例如，自定义工作单元示例
   
   ```bash
   ros2 launch my_elite_robot_cell_control start_robot.launch.py use_fake_hardware:=true
   ```

6. 你可以使用 [Elite Robots ROS2 教程](./tutorials/Elite Robots ROS2 教程.md) 以获得更多有用的信息。