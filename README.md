# R_PX0-autonomous-robot
ROS-based simulation of the R_PX0 autonomous mobile robot with 3D URDF, Gazebo environment, SLAM config, and SolidWorks design files.
## 🧠 Project Overview

- **Framework**: ROS Noetic
- **Simulation**: Gazebo / RVIZ
- **Robot Description**: URDF + STL 3D mesh files
- **SLAM**: Included (`slam.launch`, maps folder)
- **CAD**: Full 3D design in SolidWorks (.SLDPRT and .SLDASM)
```bash

## 🧪 How to Launch

Make sure to have ROS Noetic and Gazebo installed.

```bash
# Clone the repository into your ROS workspace
cd ~/catkin_ws/src
git clone https://github.com/ahmedriaahi/r_px0-autonomous-robot.git

# Build the workspace
cd ~/catkin_ws
catkin_make

# Source the workspace
source devel/setup.bash

# Launch RViz with the robot model
roslaunch r_px0 display.launch

# Launch simulation in Gazebo
roslaunch r_px0 gazebo.launch

# Launch SLAM 
roslaunch r_px0 slam.launch
```
<p align="center">
  <img src="images/Screenshot from 2025-05-26 22-56-04.png" alt="Gazebo Simulation" width="50%" style="margin-right: 10px;"/>
  <img src="SOLIDWORKS/Screenshot 2025-05-25 233130.png" alt="conception in SOLIDWORKS" width="42%"/>
<p align="center">
 <img src="images/Screenshot from 2025-05-25 22-53-19.png"  alt="RViz" width="500"/>


