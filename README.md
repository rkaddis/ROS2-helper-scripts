# ROS2 Helper Scripts
Helper scripts that make ROS2 development less annoying

## Setup
### Step 1: Clone the Repository
Clone the repository into a convienent location (I use my ROS2 workspace directory):
``` bash
git clone https://github.com/rkaddis/ROS2-helper-scripts.git
```

### Step 2: Add the directory to PATH
Adding the script directory to PATH will allow you to run the scripts in any directory.
``` bash
export PATH=$PATH:<path to this repository>
```
You can add this line to your ~/.bashrc file to automatically run on every new terminal.

### Step 3: Set the ROS2_WORKSPACE Environment Variable
Some scripts need to know the location of the ROS2 workspace, which is done through the ROS2_WORKSPACE environment variable. You can set this variable with the following line:
``` bash
export ROS2_WORKSPACE=<path to ros2 workspace>
```
You can add this line to your ~/.bashrc file to automatically run on every new terminal.

## Usage
### ros2build
#### Syntax
```
ros2build [-h] [packages to build]
```
#### Description
Builds the specified packages with `colcon build`, then sources the workspace setup file. If no packages are specified, all packages in the workspace will be built.
<br><br>

### ros2core
#### Syntax
```
ros2core [-h]
```
#### Description
Starts the rmw_zenoh_cpp router. Essentially just an alias for `ros2 run rmw_zenoh_cpp rmw_zenohd`.
