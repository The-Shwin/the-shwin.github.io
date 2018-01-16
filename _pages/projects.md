---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

Here are some selected projects.

Computer Vision
======
* <a href="https://github.com/The-Shwin/Siamese-Face-Matching">Siamese Network Face Matching</a>
  * Implemented in Python. 
  * Using PyTorch, I developed a siamese network that can process pairs of images and detect if they are a match or not. 
  * There were two versions I had for training, one used binary cross-entropy and the other used constrastive loss. In my github repository the file named p1a uses the BCE loss for training, while p1b trains models using contrastive loss. The input to the siamese network would be a text a file with a list of image pairs and whether or not a given pair was a match (used to reduce loss for training and determine accuracy when testing models). 

* Augmented Webcam Experience
  * Implemented in Matlab. 
  * Developed an augmented webcam experience. We implemented finger detection and tracking use binary morphological operators to process the frames of live video from the webcam. 
  * In order to prevent the face from interfering with the hand, we implemented a cascading object detector to detect the eyes of the face every 90 frames, and we used the the Kanade-Lucas-Tomasi feature tracking algorithm to track the salient features around the eyes in between every re-detection of the eyes. 
  * This kept the computational cost rather low so we could run eye tracking and finger tracking simultaneously.  
  * In addition, we used the location of the eyes to add filters to the user's face based on the number of fingers they were holding up, forming gesture based interaction. 
  * [Paper](https://theshwin.com/files/cvproject.pdf) - Written for the final project of my Computer Vision course. 
  
Robot Sensors & Actuators
======
* [Obstacle-Avoiding Car](https://github.com/mattkae/Obstabot)
  * Implemented in Arduino.
  * Built a small robotic car that uses and Arduino Uno and ultrasonic sensors to detect and avoid obstacles. Also attached a Bluetooth module to the Arduino Uno that lets a user communicate with the car over Bluetooth. The user can switch between autonomous control, where the car drives around and avoids obstacles, and manual control, where they override obstacle avoidance and can send directions to the car via an Android phone.
  * [Report](https://theshwin.com/files/rsaproject.pdf) - This project was built for a final project for the Robot Sensors & Actuators course that I took.

FPGA Synthesis Lab
======
* [FPGA-based Logic Analyzer](https://github.com/The-Shwin/FPGA-LogicAnalyzer)
  * Implemented in VHDL. 
  * This project was done for my FPGA Synthesis Lab course. 
  * By instantiating RAM, I used my FPGA to analyze signals. In the project, I read signals from a PIC microcontroller, but this can be extended to read external and internal signals by adjusting the .ucf file. 
  * The RAM was necessary in order to sample enough of a signal to actually see what it was doing. 
  * In the part, that I have on github, I have multiplied the FPGA internal clock by 4. This allows the logic analyzer to properly sample signals with higher frequencies. I haven't uploaded the other parts because this was a class assignment. 
  
Independent Study/Research at JHU LCSR: Autonomous Systems, Control, and Optimization Lab
======
* Motion-based Teleoperation of Robotic Arm via Razer Hydra Controller
  * Implemented in C++ with Robotic Operating System (ROS). 
  * Wrote a ROS package to send the position data of the Razer Hydra Controller and used kinematic transforms to transform the position of the Hydra controller to the frame of the end-effector of the robotic arm. 
  * This allowed the user to move their Hydra controller and have the robotic arm mimic the same movement, resulting in intuitive teleoperation of the arm without a complicated interface.
[![Hydra Teleoperation](/images/Video1.PNG)](https://drive.google.com/open?id=0Bx6eCdlCBKvvWEhiOW5EaWxNc1E)
* FPV Motion-based Teleoperation 
  * To further build on the motion-based teleoperation, I setup an FPV camera and used the DJI Lightbridge to send the video signal to an FPV headset. Now the user could operate the robotic arm via the Razer Hydra without being directly next to it to see what the arm was doing. 
  * I did not have the setup to get a good splitscreen demo of the user and the arm, but I have short video showing some of the FPV view, user operation, and arm movement. 
[![FPV Teleoperation](/images/Video2.PNG)](https://drive.google.com/file/d/1CmU1g7jDb5s4es92wabqm8_3vDx1AL4h/view)
