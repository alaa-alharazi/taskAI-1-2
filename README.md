# taskAI-1-2
## task1 install ros in ubuntu
### set locale
```
1. locale
2. sudo apt update && sudo apt install locales
3. sudo locale-gen en_US en_US.UTF-8
4. sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
5. export LANG=en_US.UTF-8
6. locale
```
### setup sources

 ```
7. apt-cache policy | grep universe
     500 http://us.archive.ubuntu.com/ubuntu jammy/universe amd64 Packages
        release v=22.04,o=Ubuntu,a=jammy,n=jammy,l=Ubuntu,c=universe,b=amd64
  ```
  
### enable the Universe repository
```
8. sudo apt install software-properties-common
   sudo add-apt-repository universe
  ```
### add the ROS 2 apt repository to your system
```
9. sudo apt update && sudo apt install curl gnupg lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```
### add the repository to your sources list.
```
10. echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
### install ROS2 packages
```
11. sudo apt update
12. sudo apt upgrade
```
### desktop install
```
13. sudo apt install ros-humble-desktop
```
### Set up your environment
```
14. source /opt/ros/humble.setup.bash
```
### try some example
```
15. source /opt/ros/humble.setup.bash
    ros2 run demo_nodes_cpp talker
```
 #### in new terminal window
```
16. source /opt/ros/humble.setup.bash
    ros2 run demo_nodes_cpp listener
```



##task2 install ROS in Jetson Nano

```
1. git clone https://github.com/JetsonHacksNano/installROS.git
2. cd instalROS/
3. ./installROS.sh
4. ./installROS.sh -p ros-melodic-desktop
```

### setup catkin Workspace
```
5. ./setupCatkinWorkspace.sh
6. gedit ~/.bashrc
7. source ~/.bashrc
8. roscore
```

### try if it is work
```
9. rostopic list
```
