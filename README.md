### How to install ROS on Jetson nano: 

##### You can install ROS (Robotics Operating System) on Jetson Nano using the following steps:

* 1. Install the operating system:
   - Install JetPack on Jetson Nano.
   - You can find JetPack on the NVIDIA Developer website and download and install it on the Jetson Nano.

* 2. Install ROS:
   - After successfully installing JetPack, you can start installing ROS.
     
   * - Open a terminal window on the Jetson Nano or connect to your device remotely using SSH.
   * - Execute the following commands to install ROS on Jetson Nano:
 ```
sudo apt-get update
sudo apt-get install -y build-essential
sudo apt-get install -y cmake git

# تثبيت ROS
sudo apt-get install -y ros-melodic-desktop-full

# تهيئة مسارات ROS
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc

# تثبيت أدوات إدارة حزم ROS
sudo apt-get install -y python-rosdep python-rosinstall python-rosinstall-generator python-wstool
sudo rosdep init
rosdep update
```


* 3. ROS installation test:
   -After you finish installing the ROS, you can test it to make sure it is working properly.

   * - Execute the following command to run the "turtlesim" example in ROS:
```
roscore
```


* In a new terminal window:
```
rosrun turtlesim turtlesim_node
```

* A new window will launch showing a turtle moving in a graphical environment.

With this, you have successfully installed ROS on Jetson Nano. You can now start developing and testing ROS applications on the device.
