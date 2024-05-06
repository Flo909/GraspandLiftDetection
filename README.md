## GraspandLiftDetection
# Project Description:
This project (based on a kaggle competition) aims to identify when a hand is grasping, lifting, and
replacing an object using EEG data that was taken from healthy subjects as they performed these
activities. The dataset contains a set of EEG recordings of 12 subjects performing grasp-and-lift
(GAL) trials. The participant’s task in each trial is to reach for a small object, grasp it using their
index finger and thumb, and lift it a few centimetres up in the air, hold it stably for a couple of
seconds, and then replace and release the object. A detailed description of the dataset can be found
from here. There are 10 series of trials for each subject and approximately 30 trials within each
series. Your task is to detect the following 6 events based on the EEG data
1. HandStart
2. FirstDigitTouch
3. BothStartLoadPhase
4. LiftOff
5. Replace
6. BothReleased

# What to do
Step 1: Download the data:  
Download the train.zip file from https://www.kaggle.com/c/grasp-and-lift-eeg-detection/data and
explore the dataset.  
This file contains the first 8 series for each subject. (We will be only using
train.zip for the project.)
There are two files for each subject + series combination:  
- the *_data.csv files contain the raw 32 channels EEG data (sampling rate 500Hz)
- the *_events.csv files contains the ground truth frame-wise labels for all events  

Step 2: Train test split:  
Split the data inside train.zip into train and test sets. You can take the first 6 series of each subject to
be your training set and 7th and 8th series to be the test set.

Step 3: Preprocess the data  
Explore on EEG signal preprocessing methods and make choices on what sort of preprocessing this
dataset would need. You can justify your choices in the report

Step 4: Decide on the neural network architecture that would be most suitable for an analysis like
this.

Step 5: Decide on the loss function and the metrics to be used in the training

Step 6: Divide the training data into train and validation sets. Implement the neural network
architecture. Train the model while tuning the hyperparameters as needed. 

Step 7: Evaluate the network using the test set. Plot AUC score for each class

Step 8 (Optional) - You can implement other deep neural networks and compare your results
# Expected Outcome
- An event detection model with acceptable results on the test set
- A table comparing the 10 best hyperparameter combinations you have attempted with their
obtained results
- A table comparing multiple neural networks architectures (if you manage to complete Step 8)
