# AL-Task-2

# Install arduino robot arm on ROS by using ubuntu 18.04

after installing ROS on ubuntu 18.04 now we can run it

Note: If You Didn't Install it yet, you can use the link and follow each step

http://wiki.ros.org/melodic/Installation/Ubuntu

# to run the ROS we need to use the next command:

```bash
$ roscore
```

and the terminal should be like this:

![2022-08-08 (2)](https://user-images.githubusercontent.com/109688999/183508938-c8326234-d780-40e7-80d6-efe05116f26d.png)

# Install the package for arduino robot arm


to Install the robot arm package you need to follow the next steps:


```bash
$ sudo apt-get install ros-noetic-catkin
```

```bash
$ mkdir -p ~/catkin_ws/src
```

```bash
$ cd ~/catkin_ws/
```

```bash
$ catkin_make
```

```bash
$ cd ~/catkin_ws/src
```

```bash
$ git clone https://github.com/smart-methods/arduino_robot_arm.git
```

```bash
$ cd ~/catkin_ws
```


# Dependencies

run this instruction inside your workspace:

```bash
$ rosdep install --from-paths src --ignore-src -r -y
```

make sure you installed all these packages:

```bash
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
```

# links that might help

you can use the following likn if you faced any trouble 

https://www.youtube.com/watch?v=fr6TXEd2rXI&t=513s&ab_channel=%D8%A7%D9%84%D8%A7%D8%B3%D8%A7%D9%84%D9%8A%D8%A8%D8%A7%D9%84%D8%B0%D9%83%D9%8A%D8%A9

# launching

now you supposed to be able to run it by using the next line:

```bash
$ roslaunch robot_arm_pkg check_motors.launch
```

# Controlling by Moveit and kinematics:

you can Control the robot arm Moveit and kinematics by using the next line:

```bash
roslaunch moveit_pkg demo.launch
```

![2022-08-09 (2)](https://user-images.githubusercontent.com/109688999/183514159-f6fd44e6-3d5c-4687-9bee-fabecc6d9650.png)



