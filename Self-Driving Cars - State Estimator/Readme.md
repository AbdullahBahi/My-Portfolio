

# Self-Driving Cars - State Estimator

In this project, I implemented [Error-State Extended Kalman Filter (**ES-EKF**)](https://ieeexplore.ieee.org/document/4420951) to localize a vehicle using data from the [CARLA simulator](https://carla.org/).   

![img](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Self-Driving%20Cars%20-%20State%20Estimator/0.PNG?raw=true)

The project has three parts completed in sequence:  

1.  First, we fill in the skeleton implementation of the ES-EKF that is provided, by writing code to perform the filter prediction step and the correction step. The filter relies on IMU data to propagate the state forward in time, and GPS and LIDAR position updates to correct the state estimate. For Part 1 of the project, the sensor data have been prepackaged - it is possible to visualize the output of the estimator and compare it to the ground truth vehicle position (the ground truth position data are also provided as shown below). 

	![1](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Self-Driving%20Cars%20-%20State%20Estimator/1.PNG?raw=true)

	The complete filter implementation is tested by comparing the estimated vehicle position (produced by our code) with the ground truth position, for a 'hold out' portion of the trajectory (i.e., for which ground truth is not provided).

	![2](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Self-Driving%20Cars%20-%20State%20Estimator/2.PNG?raw=true)
    
2.  In Part 2, we examine the effects of sensor calibration on the vehicle pose estimates. Specifically, we add a block of code that intentionally alters the transformation between the LIDAR sensor frame and the IMU sensor frame; we notice that the use of the incorrect transform results in errors in the vehicle position estimates.
	
	![3](https://github.com/AbdullahBahi/My-Portfolio/blob/master/Self-Driving%20Cars%20-%20State%20Estimator/3.PNG?raw=true)
	
	After looking at the errors, our task was to determine how to adjust the filter parameters (noise variances) to attempt to compensate for these errors. The filter code itself should remain unchanged. The updated filter (with the new parameter(s)) is tested in the same way as in Part 1.
    
3.  In Part 3, we explore the effects of sensor dropout, that is, when all external positioning information (from GPS and LIDAR) is lost for a short period of time. For Part 3, we load a different dataset where a portion of the GPS and LIDAR measurements are missing. The goal of Part 3 is to illustrate how the loss of external corrections results in drift in the vehicle position estimate, and also to aid in understanding how the uncertainty in the position estimate changes when sensor measurements are unavailable.