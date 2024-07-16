# environment setup
### move to where you install ros2 to check "setup.bash"
```
cd /opt/ros/humble/
```
 then you can see setup.bash

### Sourcing the setup script
 For each terminal, you need to run this code below ( you can see more easy way later)
```
source /opt/ros/humble/setup.bash
```
to avoid running this command everytime, add this code in bashrc
```
gedit ~/.bashrc
``` 
and add "source source /opt/ros/humble/setup.bash" at the end of line

##### check you can see return instead of "command not found"
```
ros2
```

# create workspace and directry

src is a directory
```
mkdir <workspace_name>
cd /workspace_name
mkdir src
colcon build
```

add setup.bash in bashrc file 
to check this  -.bash, go to /install and find setup.bash
then open bashrc file and add code below

```
source ~/<workspace_name>/install/setup.bash
```

# create package
 
#### we also need to decide python package or c++ package
 move to src
```
ros2 pkg create <package_name> --build-type ament_python --dependencies rclpy
```
#### ament_python is for python
#### ament_cmake is for c++

ament is to build system
rclpy is a node <this is a pythin libraray for ros2>
dependencies r the packages and funtionalities that we are going to need to use in this package

each package can contain many nodes
each node will be specific to this subpart
example: package name is <my_robot_controller>, then nodes will be specific to the control of the robot

Check that you successfully create package 


