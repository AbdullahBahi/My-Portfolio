
# Self-Driving Vehicle Controller
  
## Project Overview  
In this project, I wrote and implemented a controller for the [CARLA simulator](https://carla.org/). The goal is to control a vehicle to follow a race track by navigating through preset waypoints. The vehicle needs to reach these waypoints at certain desired speeds, so both longitudinal and lateral control will be required.  
  
## Project Specifications  
In this project, I implemented a simple controller in Python and used it to drive a car around a track in [CARLA simulator](https://carla.org/). The track is a loop shown below.

![figure](https://github.com/AbdullahBahi/Building-Full-Self-Driving-Car-Software-stack/blob/master/Course_1_Final_Project_Vehicle_Control/figure.PNG?raw=true)

The simulator offers a sorted list of waypoints which are equally spaced on this track. The waypoints include their positions as well as the speed the vehicles should attain. As a result, the waypoints become the reference signal for the controller and navigating to all the waypoints effectively completes the full track.  
  
Since the controller reference contains both position and speed, I implemented both:
- longitudinal control - [PID controller](https://ieeexplore.ieee.org/document/1453566)
- lateral control - [Stanley controller](http://ai.stanford.edu/~gabeh/papers/hoffmann_stanley_control07.pdf).
  
The controller system outputs the following commands:  
-  **Throttle**.
- **Brake**.
- **steering angle**.

The throttle and brake come from the longitudinal speed control and the steering comes from the lateral control. 

## Simulation in Action
You can click on the image below and see the simulation running

[![img](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Self-Driving%20Cars%20-%20Controller/0.png?raw=true)](https://youtu.be/SwaFDSyjZF0).

## Project repository
View source code for this project from [here](https://github.com/AbdullahBahi/Full-Software-Stack-For-Self-Driving-Cars/tree/master/Course_1_Final_Project_Vehicle_Control).