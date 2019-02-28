# Software Systems Engineering Project

## Requirements
In a home of a given city (e.g. Bologna), a ddr robot is used to clean the floor of a room (R-FloorClean).
The floor in the room is a flat floor of solid material and is equipped with two sonars, named sonar1 and sonar2 as shown in the picture (sonar1 is that at the top). 
The initial position (start-point) of the robot is detected by sonar1, while the final position (end-point) is detected by sonar2.

![Alt text](/latex/img/virtualRobot.jpg)

The robot works under the following conditions:
1. R-Start: an authorized user has sent a START command by using a human GUI interface (console) running on a conventional PC or on a smart device (Android).
2. R-TempOk: the value temperature of the city is not higher than a prefixed value (e.g. 25 degrees Celsius).
3. R-TimeOk: the current clock time is within a given interval (e.g. between 7 a.m and 10 a.m).

While the robot is working:
* it must blink a Led put on it, if the robot is a real robot (R-BlinkLed).
* it must blink a Led Hue Lamp available in the house, if the robot is a virtual robot (R-BlinkHue).
* it must avoid fixed obstacles (e.g. furniture) present in the room (R-AvoidFix) and/or mobile obstacles like balls, cats, etc. (R-AvoidMobile).
Moreover, the robot must stop its activity when one of the following conditions apply:
1. R-Stop: an authorized user has sent a STOP command by using the console.
2. R-TempKo: the value temperature of the city becomes higher than the prefixed value.
3. R-TimeKo: the current clock time is beyond the given interval.
4. R-Obstacle: the robot has found an obstacle that it is unable to avoid.
5. R-End: the robot has finished its work.

During its work, the robot can optionally:
* R-Map: build a map of the room floor with the position of the fixed obstacles. Once built, this map can be
used to define a plan for an (optimal) path form the start-point to the end-point.
