
# Obstacle Avoiding Robot using Arduino  

## Description
This project is aimed in making a Robot which detects any unexpected obstacles around it and follows the path with greatest distance from obstacles. 
Using an external trigger signal, the Trig pin on ultrasonic sensor is made logic high for at least 10µs. A sonic burst from the transmitter module is sent. 
This consists of 8 pulses of 40KHz. The signals return back after hitting a surface and the receiver detects this signal. The Echo pin is high from the time of sending the signal and receiving it. This time can be converted to distance using appropriate calculations. 
When the robot is turned on both the motors will run normally, and the robot moves forward, the ultrasonic sensor continuously calculates the distance between the robot and the reflective surface. 
If the distance between the robot and the obstacle is less than 15 cm the robot stops and scans in left and right directions, whichever side has the largest distance calculated by the ultrasonic sensor the servo motor turns it to that side and the robot moves in that direction. 
First it backs up when an obstacle is found then creates room to turn, this process continues forever and the robot keeps on moving without hitting any obstacle. The Ultrasonic sensor should not be connected directly to power supply as it might affect the normal performance. 
Instead of ultrasonic sensor, an IR transmitter – receiver pair can also be used.


Hardware Required

    Arduino Uno  [Buy Here]
    Ultrasonic Range Finder Sensor – HC – SR04  
    Motor Driver IC – L293D  [Buy Here]
    Servo Motor (Tower Pro SG90)  
    Geared Motors x 2 
    Robot Chassis  
    Power Supply 
    Battery Connector
    Battery Holder

## Circuit Diagram 
![](https://www.electronicshub.org/wp-content/uploads/2015/12/Obstacle-Avoiding-Robot-using-Arduino-Circuit-1.jpg)
## Project Gif
![](https://raw.githubusercontent.com/HHP007/first_repo/master/ezgif-3-41d059f2a5.gif)

The web link for the detailed description of the project: [Obstacle Avoiding Robot using Arduino](https://www.electronicshub.org/obstacle-avoiding-robot-arduino/)