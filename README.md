# Install and run the arm package on the ROS system

I downloaded VirtualBox, then I downloaded Ubuntu, then installed the ROS system, installed the robotic arm package, and wrote these commands to simulate the arm in RVIZ

![Task_1](https://user-images.githubusercontent.com/85695324/122712582-c9456000-d26c-11eb-91b9-1a8ecc2d9535.jpg)

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
 
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
 
sudo apt-get update
 
sudo apt-get install ros-melodic-desktop-full
 
apt-cache search ros-melodic
 
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
 
source ~/.bashrc
 
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
 
sudo apt install python-rosdep
 
sudo rosdep init
 
rosdep update
 
sudo apt-get install ros-noetic-catkin
 
mkdir -p ~/catkin_ws/src
 
cd ~/catkin_ws/
 
catkin_make
 
cd ~/catkin_ws/src
 
git clone https://github.com/smart-methods/arduino_robot_arm.git
 
cd ~/catkin_ws
 
rosdep install --from-paths src --ignore-src -r -y
 
sudo apt-get install ros-melodic-moveit
 
sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
 
sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
 
sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
 
sudo nano ~/.bashrc

source ~/.bashrc
 
roslaunch robot_arm_pkg check_motors.launch

and wrote these codes to simulate the arm in Gazebo program
Add the "arduino_robot_arm" package to "src" folder 
$ cd */catkin_ws/src 
$ sudo apt install git 
$ git clone https://github.com/smart-methods/arduino robot arm Install all the dependencies 
$ cd ~/catkin_ws 
$ rosdep ínstall --from-paths src --ignore-src -r -y 
$ sudo apt-get install ros-melodic-moveit 
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui 
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher 
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control Compile the package $ catkin_make
