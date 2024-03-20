# IoT-Enhanced Drowsiness Detection System for IT Employees: Boosting Productivity with AI and Wearable Technology
 
# Overview
Our project introduces an innovative solution to enhance the productivity and well-being of IT employees through the integration of Artificial Intelligence (AI) and Internet of Things (IoT). We present a real-time drowsiness detection system that leverages AI algorithms and wearable technology to detect signs of drowsiness and alert the individual accordingly.

# System Architecture 
![image](https://github.com/Snig17/IoT-Enhanced-Drowsiness-Detection-System-for-IT-Employees/assets/127118518/25d568db-da90-4ab6-9da9-0d1ac7fd865d)

# Methodology
##The methodologies used in this code are as follows:

### a) Eye Aspect Ratio (EAR):

Calculates the ratio of distances between certain landmarks on the eyes to detect blinking.
Utilizes the Euclidean distance to measure the distance between key points on the eyes.

### b)Final Eye Aspect Ratio (final_ear):

Calculates the average EAR for both eyes.
Combines the EAR calculation for the left and right eyes to get a more robust measure of eye openness.

### c) Lip Distance:

Measures the vertical distance between the upper and lower lips to detect yawning.
Utilizes the Euclidean distance to measure the distance between specific lip landmarks.

### d)Face Detection (Haar Cascade Classifier):

Utilizes a pre-trained cascade classifier to detect faces in the video frames
Employs the Viola-Jones object detection framework to detect faces efficiently.
Provides bounding boxes around detected faces.

### e)Facial Landmark Detection (dlib's shape predictor):

Detects facial landmarks such as eyes, nose, mouth, etc.
Uses the dlib library's pre-trained shape predictor model to locate these landmarks.
Provides precise coordinates for various facial features.

### f) Convex Hull:

Identifies the convex hull of the eyes to visualize and analyze eye regions.
Utilizes the Convex Hull algorithm to find the smallest convex polygon that encloses the eye landmarks.

### g)Alarm System:

Triggers an alarm (beep sound) when drowsiness or yawning is detected.
Utilizes the Pygame library to play audio files for the alarm sound.
Implements multithreading for continuous monitoring while the alarm is active.
Uses the espeak command-line tool to generate spoken alerts for additional auditory feedback.

### h)Arduino Integration:

Sends signals to an Arduino board connected via serial communication to trigger external actions (such as turning on a fan) based on detected events.
Uses the PySerial library to establish communication with the Arduino board and send data over the serial port.

