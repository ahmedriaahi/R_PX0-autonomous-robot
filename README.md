# R_PX0-autonomous-robot
ROS-based simulation of the R_PX0 autonomous mobile robot with 3D URDF, Gazebo environment, SLAM config, and SolidWorks design files.
## 🧠 Project Overview

- **Framework**: ROS Noetic
- **Simulation**: Gazebo / RVIZ
- **Robot Description**: URDF + STL 3D mesh files
- **SLAM**: Included (`slam.launch`, maps folder)
- **CAD**: Full 3D design in SolidWorks (.SLDPRT and .SLDASM)

## 🗂️ Project Structure
PX.0/
├── r_px0/
│   ├── CMakeLists.txt
│   ├── package.xml
│   ├── config/
│   ├── launch/
│   ├── maps/
│   ├── meshes/
│   ├── urdf/
│   ├── worlds/
│   ├── images/
│   └── export.log, frames.pdf, frames.gv
└── SOLIDWORKS/
    └── fichiers CAO (.SLDPRT, .SLDASM) + captures

## 🧪 How to Launch

Make sure to have ROS (e.g., Noetic) and Gazebo installed.

```bash
# Clone the repository into your ROS workspace
cd ~/catkin_ws/src
git clone https://github.com/yourusername/r_px0-autonomous-robot.git

# Build the workspace
cd ~/catkin_ws
catkin_make

# Source the workspace
source devel/setup.bash

# Launch RViz with the robot model
roslaunch r_px0 display.launch

# Launch simulation in Gazebo
roslaunch r_px0 gazebo.launch

# Launch SLAM (if configured)
roslaunch r_px0 slam.launch
```
