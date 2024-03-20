# IoT-Enhanced Drowsiness Detection System for IT Employees: Boosting Productivity with AI and Wearable Technology
 
# Overview
Our project introduces an innovative solution to enhance the productivity and well-being of IT employees through the integration of Artificial Intelligence (AI) and Internet of Things (IoT). We present a real-time drowsiness detection system that leverages AI algorithms and wearable technology to detect signs of drowsiness and alert the individual accordingly.

# System Architecture 
![image](https://github.com/Snig17/IoT-Enhanced-Drowsiness-Detection-System-for-IT-Employees/assets/127118518/25d568db-da90-4ab6-9da9-0d1ac7fd865d)

# Methodology
## The methodologies used in this code are as follows:

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

# Implementation

### Step-1 : Setup Hardware:

Acquire necessary hardware components including a webcam for video input and an Arduino board for interfacing with external devices.

### Step-2: Install Dependencies:

Install required libraries and dependencies including OpenCV, dlib, imutils, Pygame, and PySerial.

### Step-3: Define Constants and Thresholds:

Set thresholds for eye aspect ratio (EAR), consecutive frames for drowsiness detection, and yawning distance threshold.

### Step-4: Load Models:

Load the pre-trained Haar Cascade classifier for face detection and dlib's shape predictor model for facial landmark detection.

### Step-5:Initialize Video Stream:

Start the video stream from the webcam using OpenCV or imutils.

### Step-6: Main Loop:

Continuously capture frames from the video stream.

### Step-7:Face Detection:

Use the Haar Cascade classifier to detect faces in each frame.
Draw bounding boxes around detected faces.

### Step-8: Facial Landmark Detection:

For each detected face, use the shape predictor to locate facial landmarks such as eyes and lips.
Calculate the eye aspect ratio (EAR) and lip distance for drowsiness and yawning detection, respectively.

### Step-9: Eye Blink Detection:

If the calculated EAR falls below the threshold for a certain number of consecutive frames, trigger a drowsiness alert.
Play an alarm sound and send a signal to the Arduino board to activate external alerts (e.g., LED lights or a buzzer).

### Step-10:Yawn Detection:

If the lip distance exceeds the predefined threshold, trigger a yawn alert.
Play an alarm sound and send a signal to the Arduino board for external alerts.

### Step- 11: Multithreading for Alerts:

Utilize multithreading to handle concurrent tasks such as playing audio alerts and sending signals to the Arduino board.

### Step-12: Terminate Program:

Allow the user to terminate the program by pressing a designated key (e.g., 'q’).

### Step-13: Cleanup:

Release video stream resources and close any open windows before terminating the program.

### Step-14: Arduino Integration:

Establish serial communication with the Arduino board and send appropriate signals based on detected events (e.g., drowsiness or yawning).
Implement Arduino code to receive signals and trigger external alerts or actions.

### Step-15: Testing and Optimization:

Test the system with different scenarios and adjust thresholds or parameters for optimal performance.
Optimize the code for efficiency and reliability, considering factors such as frame rate and processing speed.
