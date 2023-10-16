# Warehouse-Assistance-AGV
A vision based 2-wheel drive robot which navigates based on detected directional aids and Aruco markers using OpenCV on Raspberry pi and Properller embedded system for 360degrees continuous servo motor control.
Utilization of Ultrasonic sensors for widget detection and IR sensors for path guidance.

<img src = "https://github.com/PranayG/Warehouse-Assistance-AGV/assets/9202531/4999f083-7387-4bbe-b05c-6956dd1c590d" width = "250" height ="350">


# Project Objective

The primary objective of our project is to develop a robot capable of autonomously navigating the warehouse floor while accurately counting defective and non-defective widgets. 

## Navigation Strategy

The robot will rely on directional aids, such as triangular markers, strategically placed throughout the warehouse to make informed turn decisions. By following these directional aids, the robot will seamlessly maneuver through the warehouse's three major sections, ensuring it covers the entire inventory space.
Upon reaching this destination, the robot will display the final count of defective and non-defective widgets, providing warehouse management with accurate and up-to-date inventory information.

## Methodology
The robot line follows and senses a direction (right or left) using image processing and will blink an LED 
to detect an intersection. The moment it senses an obstacle it searches for an Aruco marker to detect that it 
needs to pick up a defective or a non-defective widget and stores it. It continues to do the same for the next 
three iterations in the warehouse and finally reaches the docking station.
At the docking station , using Computer Vision it detects the direction of the triangle again and rotates 
along the same direction until it sense an Aruco marker . Once it senses the aruco marker it goes to the 
docking station and unloads all the widget by displaying the total number of defective and non-defective
widgets

| S no. | Name of the part                      | Qty |
|-------|--------------------------------------|-----|
| 1     | Parallax Propeller                  | 1   |
| 2     | Ultrasonic Sensor – HCSR04          | 2   |
| 3     | Infrared Sensor                     | 3   |
| 4     | LEDs: Orange                        | 3   |
| 5     | Parallax continuous servo motors    | 2   |
| 6     | 3D printed PLA Chassis and mount    | 1   |
| 7     | Jumper Wires                        | 50  |
| 8     | LCD Display                         | 1   |
| 9     | 9-V Battery                         | 2   |
| 10    | Raspberry Pi                        | 1   |
| 11    | Web-camera                          | 1   |
| 12    | Buck Converter                      | 1   |
| 13    | Wheels                              | 2   |


## Schematics
<img src = "https://github.com/PranayG/Warehouse-Assistance-AGV/assets/9202531/c8435511-a6d6-404e-9612-92b67a265e95" width = "450" height ="350">

## Flowchart
![image](https://github.com/PranayG/Warehouse-Assistance-AGV/assets/9202531/208e771c-f377-4113-8243-c7df54c780c5)

## Chassis

<img src = "https://github.com/PranayG/Warehouse-Assistance-AGV/assets/9202531/d4e52445-5329-416d-822b-f89f1fd1bc40" width = "300" height ="250">

The design is 3D printed to hold the Propeller Board and mount the Ultrasonic Sensor, 3 IR Sensors, and the Battery attached with the continuous servo motors. The design was modelled using Autodesk Fusion 360 and printed on the Ultimakers using the Cura software.

## Conclusion

The project demonstrates the practical application of computer vision techniques for marker detection and shape recognition. By combining the functionalities of detecting ArUco markers and triangles, the system can be used in various real-world scenarios. For example, it could be integrated into robotics or automation systems to provide visual feedback and make decisions based on detected markers or triangle orientations.

The project's implementation successfully achieves its objectives of real-time marker detection and triangle direction determination. However, there are potential areas for improvement. For instance, the code could be optimized for better performance, such as using multi-threading to parallelize the detection processes. Additionally, more robust error handling and exception management could be incorporated to enhance the reliability and stability of the system.

