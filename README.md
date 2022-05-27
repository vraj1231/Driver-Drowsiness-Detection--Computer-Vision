# Driver-Drowsiness-Detection--Computer-Vision

### Motivation 
Drowsiness detection is a car safety technology that helps prevent accidents caused by drivers who fell asleep while driving.
According to NHTSA (National Highway Traffic Safety Administration), 91,000 police-reported crashes involved drowsy drivers. These crashes led to an estimated 50,000 people injured and nearly 800 deaths in 2017.
Currently, methods are mainly focus on eye blink detection using deep learning or machine learning technologies, however, what if drivers wear sunglasses?

### Objective

In this project, we work on facial landmark detector to solve this problem.
Trained on the driver’s face, and detecting the face of the driver using a camera and analysing the state of drivers.
This detector can tell if drivers are drowsy and then offers a warning.
Aim to help reduce the amount of road accidents.
The main motivation of driver drowsiness detection can save a lot of lives, not only for drivers but also of other people who share the road with.

![image](https://user-images.githubusercontent.com/60303995/170636250-02835e09-0756-490b-a820-32fe10933455.png)


### Methodology

![image](https://user-images.githubusercontent.com/60303995/170636317-3ba2cc37-1065-48ab-8847-b56cc8f4b557.png)


### Dataset

The “ULg Multimodality Drowsiness Database” also called DROZY, is a database containing various types of drowsiness-related data (signals, images, etc.).
•The data in the DROZY database were collected from 14 young, healthy subjects (3 males, 11 females) who performed three successive 10-min psychomotor vigilance tests (PVTs) in conditions of increasing sleep deprivation induced by acute, prolonged waking.
•The dataset contains automatic and manual annotations for facial landmarks and also timestamp for each video.

 Karolinska Sleepiness Scale (KSS)

This scale measures the subjective level of sleepiness at a particular time during the day.
It has a range from 1 to 9 where 1 is rated as very alert and 9 is rated as very sleepy.
![image](https://user-images.githubusercontent.com/60303995/170636412-2812042e-6da0-472b-885f-a98c8dab73a5.png)

## Feature Extraction
•Average Blink Duration: the duration for which the eye aspect ratio is below 0.3 and then goes above 0.3 is detected as a blink. The time for which a blink happens is called blink duration. Blink duration per minute is averaged out to calculate average blink duration.
•Blink Frequency: number of blinks per minute is called blink frequency.
•Average PERCLOS (Percentage Closure): number of frames for which the eyes are closed (i.e. eye aspect ratio is below 0.3) are calculated and then PERCLOS is averaged out per minute to calculate average PERCLOS.
•Mouth Aspect Ratio: MAR is calculated to detect whether a person is yawning or not.
•Head Pose: different angles are calculated at each frame to get the head pose.
•KSS Values: the subjective, self evaluated values given by the participants were considered as the labels (the levels of drowsiness) for the extracted features.

![image](https://user-images.githubusercontent.com/60303995/170636511-ca60e652-2af9-4a49-939e-c9bcb5175af1.png)

## Conclusion
Based on the results from test data we conclude that facial landmark detector is  practical and reliable in driver drowsiness detection task.
Artificial Neural Network with 4 layers gave an accuracy of 74.5% on test data which is the best model for the system .
We have less accuracy since our dataset does not have labels frame wise or per minute in the video, due to which the accuracy is less.

