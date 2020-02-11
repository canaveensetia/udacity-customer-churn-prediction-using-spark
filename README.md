# Project Overview

The project purpose is to build a customer churn prediciton model. We analyzed user interactions with a fictious "sparkify" audio streaming service. 

Based on a history of user actions, the model has to predict whether is is likely that the user will churn or not.

# Dataset Overview

Provided data set is of 12GB describing user interactions with the service. The data is avaliable at Udacity Amazon s3 bucket: s3n://udacity-dsnd/sparkify/sparkify_event_data.json. However, for building the script subset of provided data is used.


Every log entry includes the service page user interacted with ('next song', 'thumbs up', 'settings', etc), user id, session id, user account level, and the timestamp.

# Modelling Overview

## Features

We added quite a few features to build the model 

**Thumbs Up:** The average number of 'thumbs up' given per song

**Thumbs Down:** The average number of 'thumbs down' given per song

**Songs Played:** The total number of songs played

**Number of Days:** The number of days the user had been members of the music service

**Songs Per Hour:** How many songs in an hour was played

## Target Variable

Created a target variable churn whose probability will be predicted.

## Prediction model

Post creation of feature dataset and a target variable, we split the dataset in train, validation and test parts. 

Finally, post feature scaling, Logistic Regression and Random Forest Model were trained. Random Forest Classifier worked better on relative basis.

## Results:

**Train:** Area Under ROC 0.9985119047619048

**Train:** Area Under PR 0.9942257534428728

**Validation:** Area Under ROC 0.9523809523809523

**Validation:** Area Under PR 0.9027777777777777

**Test:** Area Under ROC 0.8428030303030303

**Test:** Area Under PR 0.7930118994150303
