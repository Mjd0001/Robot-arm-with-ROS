# Robot-arm-with-ROS
Use ROS packages to control arduino robot arm with simulation.
## Robot initial positions:
Using this Arduino code, we will put initial positions for each servo as following:
Base: 90
shoulder: 90
Elbow: 90
Wrist: 90
Gripper: 0
```
#include <Servo.h> 
Servo myservo;

void setup(){
  myservo.attach(10);
  myservo.write(90);
}

void loop(){
  
}
```
## Dependencies in ROS:
### install packages:
```
sudo apt-get install ros-noetic-catkin
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```

## Install Arduino on ROS:
1- Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software , then unzipping the folder, to install run $ sudo ./install.sh .
2- chech Ariduno Bord by run Blink Example, if there is a problem in the port, try this commend: 
```
sudo chmod a+rw /dev/ttyACM0
```

