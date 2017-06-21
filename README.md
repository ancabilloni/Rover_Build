# BUILDING AN AUTONOMOUS ROVER
This is part of the capstone course in Robotics Specialization by University of Pennsylvania on Cousera.
## Part 1: Hardware Build
Parts List: https://www.adafruit.com/wishlists/402816

![img_20170504_192643](https://user-images.githubusercontent.com/23693651/27317578-5b730764-5555-11e7-99e1-de35b920827c.jpg)

Putting parts together:
![img_20170617_142307](https://user-images.githubusercontent.com/23693651/27406621-6e6db4b4-56a3-11e7-8207-7607df4245e3.jpg)

Final Assembly:
![img_20170618_021439 1](https://user-images.githubusercontent.com/23693651/27317581-60388c9c-5555-11e7-879d-6c8bbe5c8f5d.jpg)

## Part 2: Initial Set up
*Note: The Operation System using to work on this project is Ubuntu*
To get the Pi image, access to Robotics Capstone class by University of Pennsylvania in Week 2 material.
Flashing the Pi using Linux: https://www.raspberrypi.org/documentation/installation/installing-images/linux.md

### Instruction:
- Power up the Pi
- To expand the storage and using all the space in the memory card, on terminal type `sudo raspi-config` > Choose `Expand Filesystem`
- To boot in GUI mode, type `startx`
Connect the Pi to Wifi:
- In GUI, choose the wifi network that wants to connect the Pi to and save the network.
- To find the Pi's ip address, type `hostname -I`, write down the ip address name.
Connect to the Pi remotely using `ssh`:
- In terminal,type `ssh pi@<ip-address>` and provide password if asking for one.

## Part 3: Software
### Linear Test Run
- SSH to the Pi, change current directory to `/home/pi/catkin_ws/src/robot_control/src/`
- Open `RobotControl.py`, in this case, I used nano with `sudo nano RobotControl.py`
- 3 important functions to remember `self.ros_interface.get_measurements(), self.ros_interface.get_imu() and self.ros_interface.command_velocity(lin_vel, ang_vel)`
- To test run the rover, I used `self.ros_interface.command_velocity(0.3, 0)`. This will set the velocity of the rover to 30cm/s.

1st Linear Test Run Result:
https://www.youtube.com/watch?v=JKuvPJvMov0&feature=youtu.be

Up next: Camera Calibration and Motor Calibration

