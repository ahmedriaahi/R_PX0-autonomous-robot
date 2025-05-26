# R_PX0-autonomous-robot
ROS-based simulation of the R_PX0 autonomous mobile robot with 3D URDF, Gazebo environment, SLAM config, and SolidWorks design files.
## 🧠 Project Overview

- **Framework**: ROS Noetic
- **Simulation**: Gazebo / RVIZ
- **Robot Description**: URDF + STL 3D mesh files
- **SLAM**: Included (`slam.launch`, maps folder)
- **CAD**: Full 3D design in SolidWorks (.SLDPRT and .SLDASM)
```bash
📁 r_px0-autonomous-robot
 ┣ 📂 r_px0/                     # Main ROS package
 ┃ ┣ 📂 config/                 # YAML configuration files for joints and control
 ┃ ┃ ┣ 📜 control.yaml
 ┃ ┃ ┣ 📜 joint_names_R_PX0.yaml
 ┃ ┣ 📂 images/                 # Screenshots of RViz, Gazebo, and SLAM
 ┃ ┣ 📂 launch/                 # ROS launch files
 ┃ ┃ ┣ 📜 display.launch
 ┃ ┃ ┣ 📜 gazebo.launch
 ┃ ┃ ┗ 📜 slam.launch
 ┃ ┣ 📂 maps/                   # SLAM-generated map and metadata
 ┃ ┃ ┣ 📜 r_px0_map.pgm
 ┃ ┃ ┗ 📜 r_px0_map.yaml
 ┃ ┣ 📂 meshes/                 # STL files for the robot’s 3D model
 ┃ ┃ ┣ 📦 base_link.STL
 ┃ ┣ 📂 urdf/                   # Robot URDF and joint data
 ┃ ┃ ┣ 📜 R_PX0.urdf
 ┃ ┃ ┗ 📜 R_PX0.csv
 ┃ ┣ 📂 worlds/                 # Custom Gazebo world for simulation
 ┃ ┃ ┗ 📜 r_px0_world.world
 ┃ ┣ 📜 CMakeLists.txt          # Build configuration for ROS
 ┃ ┣ 📜 package.xml             # ROS package metadata
 ┃ ┣ 📜 frames.gv               # TF frame diagram source
 ┃ ┣ 📜 frames.pdf              # TF tree visualization (compiled)
 ┃ ┗ 📜 export.log              # Export logs or notes
 ┃
 ┣ 📂 SOLIDWORKS/               # 3D design files from SolidWorks
 ┃ ┣ 📦 P1.SLDPRT               # Part 1 model
 ┃ ┣ 📦 P2.SLDPRT               # Part 2 model
 ┃ ┣ 📦 R.PX0.SLDASM            # Full robot assembly
 ┃ ┣ 📷 Screenshot 2025-05-17 210221.png
```

## 🧪 How to Launch

Make sure to have ROS (e.g., Noetic) and Gazebo installed.

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
### Example: Robot in RViz
<img src="images/Screenshot from 2025-05-25 22-53-19.png" alt="RViz" width="500"/>

<p align="center">
  <img src="images/gazebo_sim.png" alt="Gazebo Simulation" width="45%" style="margin-right: 10px;"/>
  <img src="SOLIDWORKS/Screenshot 2025-05-25 233130" alt="SLAM in RViz" width="45%"/>
</p>


