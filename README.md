# Drowsiness_detection


Project Title :  Drowsiness Detection 

Problem Statement : To detect the driver is in drowsy mode or not while driving to avoid accidents by continously monitoring his eyes activity through camera and also monitor whether he is yawning or not.


Proposed methodology : We used MobileNetV3 for building the model.

MobileNetV3 first searches for a coarse architecture using MnasNet, which uses reinforcement learning to select the optimal configuration from a discrete set of choices.
After that, the model fine-tunes the architecture using NetAdapt, a complementary technique that trims under-utilized activation channels in small decrements.

Another novel idea of MobileNetV3 is the incorporation of an squeeze-and-excitation block into the core architecture. 

The core idea of the squeeze-and-excitation blocks is to improve the quality of representations produced by a network by explicitly modelling the interdependencies between the channels of its convolutional features



* Initially we build a model using MobileNetV3 to classify whether person's eye is close or not and also if he yawning or not.

* Then through opencv camera we detected face(for yawning purpose) and detected eye(for closed or open) 

* If the eyes are open it should display as open and for closed eyes it should display as closed and for yawning it should display as yawning.


Code Requirements
The example code is in Python (version 2.7 or higher will work).

Dependencies
import matplotlib.pyplot
import numpy
import os
import tensorflow


Description 
A computer vision system that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsy.

Dataset
This dataset consists of 2688 images belonging to two classes:
close:1072 images
open:563 images
yawn:1052 images
The images used were real images of people with closed and opened eyes. The images were collected from the following sources:
•	MRL Dataset
•	Custom dataset


Execution
Step 1:training the model with the appropriate data, downloading the model weights.

Step 2:running the ipynb file for testing through webcam and save the model in .h5

Step 3:from the save model .h5 to be converted to .tflite to be used for deploying it on android device.

Step 4:testing app on the edge device.


Testing :

*Run eis_drowsiness_2021.ipynb to train and test images
*Load and Run eis_drowsiness_2021.h5 model for precition using opencv(bounding box)
*Android app can be thorugh folder codelabs/drowsiness_detection/android/start/app/src

Android folder drive link

https://drive.google.com/drive/folders/1iOHi3rR3SAB-0PoJyoHJPCT3xv97M85c?usp=sharing
