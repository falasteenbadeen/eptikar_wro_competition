# AMT-Ebtikar_WRO_competition
Engineering Documentation
This repository contains engineering materials of a self-driven vehicle's model participating in the WRO Future Engineers competition in the season 2023.

# Team members:
* Hadi Nedal Bdair-email:hadibdair.00@gmail.com                                                                                                                                                                        
* Mohammad Ameen Zidan-email:mz5246076@gmail.com

# Introduction
The AMT-Ebticar vehicle is designed using two precise control units: Raspberry Pi and Arduino. The Arduino is programmed to receive accurate information from the Raspberry Pi to facilitate decision-making, avoiding obstacles. This is done using the serial library commands for Raspberry Pi, the serial monitor in Arduino, and the platform used to execute and upload the code to the Raspberry Pi is the Arduino IDE. Considering the above, two programming languages will be used for control: C++ for Arduino and Python for Raspberry Pi. Python is used with the Raspberry Pi to analyze inputs from the camera and translate the readings to determine the color and size of the object. Based on this information, the Arduino controls several ultrasonic sensors to determine the distance between the car and the wall, as well as the direction it needs to turn. This is done by controlling the steering through a servo system. When obstacles are detected, a command is sent to the motor driver to reduce the speed, facilitating the turn. The accuracy of the turn is increased by using the gyroscope sensor, which measures the angle.

# Repository Overview
* models : contains 3D Printable files designed by us
* others : other essential photos
* schemes : contains the electrical systems schematics
* src : contains the main programs and code
* t-photos : contains one serious and one funny photo
* v-photos : contains the photos of the robot from all required directions
* video : contains youtube link of the video 





