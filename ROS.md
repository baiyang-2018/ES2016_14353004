#ROS安装

##安装步骤
###Configure your Ubuntu repositories

Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." You can follow the Ubuntu guide for instructions on doing this. 

###Setup your sources.list
Setup your computer to accept software from packages.ros.org. ROS Kinetic ONLY supports Wily (Ubuntu 15.10), Xenial (Ubuntu 16.04) and Jessie (Debian 8) for debian packages. 

- sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

###Set up your keys
- sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
###Installation
First, make sure your Debian package index is up-to-date: 

- sudo apt-get update

There are many different libraries and tools in ROS. We provided four default configurations to get you started. You can also install ROS packages individually. 

In case of problems with the next step, you can use following repositories instead of the ones mentioned above ros-shadow-fixed

Desktop-Full Install: (Recommended) : ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators, navigation and 2D/3D perception

- sudo apt-get install ros-kinetic-desktop-full

Desktop Install: ROS, rqt, rviz, and robot-generic libraries 

- sudo apt-get install ros-kinetic-desktop

ROS-Base: (Bare Bones) ROS package, build, and communication libraries. No GUI tools. 

- sudo apt-get install ros-kinetic-ros-base


To find available packages, use: 

- apt-cache search ros-kinetic
###Initialize rosdep
Before you can use ROS, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS. 


- sudo rosdep init
- rosdep update

###Environment setup
It's convenient if the ROS environment variables are automatically added to your bash session every time a new shell is launched: 

- echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

If you have more than one ROS distribution installed, ~/.bashrc must only source the setup.bash for the version you are currently using.

If you just want to change the environment of your current shell, instead of the above you can type: 

- source /opt/ros/kinetic/setup.bash
###Getting rosinstall
rosinstall is a frequently used command-line tool in ROS that is distributed separately. It enables you to easily download many source trees for ROS packages with one command. 

To install this tool on Ubuntu, run: 


- sudo apt-get install python-rosinstall
###Build farm status
The packages that you installed were built by the ROS build farm.  

##安装心得
很开心装好了ROS，虽然还没有经过测试，但装的过程中至少没怎么报错。。。然后给了我一次难忘的体验：我把虚拟机装崩了！！！

![](http://p1.bpimg.com/567571/55c4cbeaa732f77d.jpg)
我去百度原因，别人的回复都是：把虚拟机装崩了,有点厉害啊！！
感觉达成了人生成就。。。完！