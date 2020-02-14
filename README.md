# Project Overview

I got an opportunity to work on the customer churn problem which is the final project of the “Udacity Data Science Nanodegree program”. We have been provided a virtual company called ‘Sparkify’ which is a music app and it offers paid and free listening service. The customer can switch between either service or they can cancel their subscription at any time.

This provided dataset contains two months of ‘Sparkify’ user behavior log. The log contains some 
basic information about the user as well as information about a single action.

The given dataset is large i.e. 12GB, thus the typical tools for analysis and machine learning will not be useful here as it will not fit in the most of the local computer’s memory. The ideal and safe way to perform such analysis is to do it using Big Data tools like Apache Spark.


## Why Apache Spark?

As mentioned above, provided dataset shared as part of this project is over 12GB so it is virtually impossible to load this into a typical development machine.
The Spark distributed analysis capability makes it relatively easy to handle these large datasets and reduce the time it takes to analyze the data and train models.

## How to save costs?
As highlighted above, it is not possible to load over 12GB in a typical local development machine. So, we can use a subset of data to explore and build a model in a local development environment.
Once it is fully tested it can be used in a cloud-based development (e.g. on Amazon AWS, Microsoft Azure, etc.) environment to run the script on full 12GB data.

## What is the outcome of the project?
As highlighted above, the business ask is to predict whether a customer will churn or not.
From the machine learning perspective, it is a binary classification problem i.e. a binary outcome whether a customer will churn or not.

## Dataset Overview

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

**Validation:** Area Under ROC 0.9047619047619048

**Validation:** Area Under PR 0.8500000000000001

**Test:** Area Under ROC 0.8579545454545455

**Test:** Area Under PR 0.826208854004175

# Medium Blog Link

https://medium.com/@setia.naveen/predict-customer-churn-in-a-distributed-way-using-spark-33dce920f7ce

# Reference(s)/Credit(s)

https://en.wikipedia.org/wiki/Customer_attrition

https://spark.apache.org/docs/latest/ml-classification-regression.html#random-forest-classifier

https://spark.apache.org/docs/latest/ml-classification-regression.html#binomial-logistic-regression
