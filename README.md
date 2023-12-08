# C-100 Robot Model

This repository contains the URDF and SDF files for the C-100, a differential drive mobile robot equipped with two LiDAR sensors.

## Robot Specifications

- **Name:** C-100
- **Type:** Differential Drive Mobile Robot
- **Length:** 721.75 mm
- **Width:** 521.75 mm
- **Height:** 200.0 mm
- **Wheel Radius:** 196.25 mm
- **Wheel Width:** 28.0 mm
- **Track Width:** 320.6 mm
- **Lidar Height from Ground:** 130.0 mm
- **Lidar Cylinder Radius:** 43.37 mm
- **Lidar Cylinder Height:** 35.0 mm
- **Front Lidar Position from Robot Wheel Line:** 198.0 mm
- **Rear Lidar Position from Robot Wheel Line:** 198.0 mm

## File Descriptions

- `c-100.urdf`: This URDF (Unified Robot Description Format) file describes the physical and visual properties of the C-100 robot for use in robot simulation environments.
- `c-100.sdf`: This SDF (Simulation Description Format) file provides a similar description as the URDF but in a format suitable for use with Gazebo and other simulation environments that support the SDF standard.

## Usage

### URDF File

The URDF file can be used in various robot simulation environments that support URDF, such as ROS (Robot Operating System). To use this file, simply load it into your simulation environment. For example, in ROS, you can 
use the `robot_state_publisher` to publish the state of the robot based on this URDF.

### SDF File

The SDF file is primarily used with the Gazebo simulation environment. To use this file in Gazebo, you can include it in your Gazebo world file or load it directly into the Gazebo environment.

## Using the C-100 Model in Gazebo

### Prerequisites

Before you begin, ensure you have Gazebo installed on your system. Gazebo is a powerful robot simulation tool widely used in the robotics community. You can download and install Gazebo from [http://gazebosim.org](http://gazebosim.org).

### Loading the Model into Gazebo

1. **Start Gazebo:** Open a terminal and launch Gazebo by typing `gazebo` and pressing Enter. This will open the Gazebo interface.

2. **Import the Model:**
   - If you have a Gazebo world file (`world_name.world`), you can include the C-100 model directly in this file. Add the following line within the `<world>` tag:
     ```xml
     <include>
       <uri>model://path_to_your_model/c100.sdf</uri>
     </include>
     ```
   - Alternatively, you can import the model directly into an existing Gazebo environment. In the Gazebo interface, click on `Insert` and navigate to the location of your `c100.sdf` file. Click on the model to add it to the simulation.

3. **Interacting with the Model:**
   - Once the model is loaded in Gazebo, you can interact with it using the Gazebo GUI. You can move the robot, simulate sensors, and observe its behavior in a virtual environment.
   - For more advanced interactions, such as controlling the robot programmatically or simulating sensor data, you will need to use additional tools like ROS (Robot Operating System).

### Advanced Usage with ROS

If you are using ROS (Robot Operating System) alongside Gazebo, you can control the C-100 robot and simulate its sensors more effectively. This requires a ROS installation and a proper setup for integrating ROS with Gazebo. You can find more information on ROS-Gazebo integration at [http://wiki.ros.org/gazebo_ros_pkgs](http://wiki.ros.org/gazebo_ros_pkgs).

## Notes

- The mass and inertia values in both URDF and SDF files are placeholders. Adjust these values according to the actual physical properties of your robot for accurate simulation results.
- Ensure that your simulation environment is properly configured to handle the dimensions and properties defined in these files.
