# Task_1_Robot_Arm
I downloaded VirtualBox, then I downloaded Ubuntu, then installed the ROS system, installed the robotic arm package, and wrote these commands to simulate the arm in RVIZ
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

and wrote these codes to emulate the Gazebo program
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gaz... `lsb_release -cs` main" ＞ /etc/apt/sources.list.d/gazebo-latest.list'
wget https://packages.osrfoundation.org/ga... -O - | sudo apt-key add -
     sudo apt-get update
     sudo apt-get install gazebo9
sudo gedit ~/.ignition/fuel/config.yaml

