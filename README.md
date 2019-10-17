# A creo cad model is converted into a urdf and tested here.

## Important Notes

1. Make sure that stl files are binary and not ASCII.
2. Make sure that the location of stl files are correct and are properly specificed like [here](https://github.com/ajaygunalan/just_mobile_base/blob/master/advr_mob_plt_description/urdf/main.urdf).
3. Make sure to have **MatLab Version** less than **2016** and generate **first generation XML files**
4. Check the URDF by: `check_urdf <urdf file>` to get something like this:
```
robot name is: MAIN
---------- Successfully Parsed XML ---------------
root Link: CHASSIS_SUB has 4 child(ren)
    child(1):  WHEEL_SUB
    child(2):  WHEEL_SUB-1
    child(3):  WHEEL_SUB-2
    child(4):  WHEEL_SUB-3
```
or use `urdf_to_graphiz <urdf file>` for pdf containing the tree structure like [this](https://github.com/ajaygunalan/just_mobile_base/blob/master/advr_mob_plt_description/urdf/MAIN.pdf).


## References

* [Robotic simulation scenarios with Gazebo and ROS](https://www.generationrobots.com/blog/en/robotic-simulation-scenarios-with-gazebo-and-ros/)
* [simmechanics-to-urdf](https://github.com/robotology/simmechanics-to-urdf)
* [How to create launch file for URDF and open in Gazebo](https://www.theconstructsim.com/ros-qa-142-how-to-create-launch-file-for-urdf-and-open-in-gazebo/)
* [Moving Joints in Gazebo Simple Example](https://www.theconstructsim.com/ros-qa-070-moving-joints-gazebo-simple-example/)
* [Tutorial on creating a ROS-enabled mobile robot in Gazebo](https://github.com/HumaRobotics/mybot_gazebo_tutorial)

## To use this package

**For visualization in RViz**

```
roslaunch advr_mob_plt_description advr_mob_plt_display.launch

```
**For visualization in Gazebo**

```
roslaunch advr_mob_plt_gazebo advr_mob_plt_world.launch
```