# Military Shot Detection System
Automatic system used for training military soldiers on shooting. The system detects successful shots on targets using Image Processing techniques then displays soldier results on a 7-segment display in real time and finally after the shooting session is over the results can be viewed and saved using a custom GUI software.

## Demo Video
Click on the image below to see a demo video of the project in the field.
[![0](.)](https://www.youtube.com/watch?v=HDt6BvZ4hAg)

## Project Overview 

The system consists of the following hardware:
- Arduino control box connected to an array of **7-segments** displays and an **NRF24L01** RF wireless module.
- Raspberry Pi connected to an HD camera to capture and process images of targets in real-time.

![1](.)

### How it works?

- The camera captures images of targets in real-time while shooting and these images are processed on the Raspberry Pi to detect successful shots on targets.   

	![3](.)
	
- The results are then sent immediately to the Arduino control box using wireless communication to be displayed on the 7-segments.
- After training session is over, the results of the session can be accessed and viewed using an easy-to-use GUI and finally the results are saved to a csv file.

	![2](.)  