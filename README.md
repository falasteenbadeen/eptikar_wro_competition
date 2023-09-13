# AMT-Ebtikar Engineering Documentation
This repository contains engineering materials of a self-driven vehicle's model participating in the WRO Future Engineers competition in the season 2023.

# Team members:
* Hadi Nedal Bdair-email:hadibdair.00@gmail.com                                                                                                                                                                        
* Mohammad Ameen Zidan-email:mz5246076@gmail.com

# Introduction
The AMT-Ebticar vehicle is designed using two precise control units: Raspberry Pi and Arduino. The Arduino is programmed to receive accurate information from the Raspberry Pi to facilitate decision-making, avoiding obstacles. This is done using the serial library commands for Raspberry Pi, the serial monitor in Arduino, and the platform used to execute and upload the code to the Raspberry Pi is the Arduino IDE. Considering the above, two programming languages will be used for control: C++ for Arduino and Python for Raspberry Pi. Python is used with the Raspberry Pi to analyze inputs from the camera and translate the readings to determine the color and size of the object. Based on this information, the Arduino controls several ultrasonic sensors to determine the distance between the car and the wall, as well as the direction it needs to turn. This is done by controlling the steering through a servo system. When obstacles are detected, a command is sent to the motor driver to reduce the speed, facilitating the turn. The accuracy of the turn is increased by using the gyroscope sensor, which measures the angle.

# Repository Overview
* models : contains 3D Printable files designed by us.
* others : other essential photos.
* schemes : contains the electrical systems schematics.
* src : contains the main programs and code.
* t-photos : contains one serious and one funny photo.
* v-photos : contains the photos of the robot from all required directions.
* video : contains youtube link of the video. 


# Power and Sense management
We used two batteries, one responsible for supplying power to the Raspberry Pi for analysis, and one responsible for supplying power to the Arduino for motion. The capacity of these batteries is 11 volts each, and the robot can operate continuously for approximately twenty minutes.


# Program arrangement and Algorithm Planning
The camera captures images at a speed of 20 frames per second and identifies red or green color through converting the reading system from RGB to HSV. It then creates a mask for the green and red colors, distinguishing them from other paths or rings. It further discerns between the closest and farthest cubes and their respective colors. The decision-making process to avoid obstacles is as follows: upon seeing the green cube, the direction is adjusted to the right to avoid the obstacle. In contrast, when the red cube is detected, the direction is adjusted to the left to avoid the obstacle. If the camera doesn't detect any cube, information is sent to the Arduino using the serial library to make a decision on avoiding external or internal obstacles based on the readings from the ultrasonic sensors. After making the turn, the gyroscope measures the angle of the turn and adjusts the robot's path to travel in a straight line.




