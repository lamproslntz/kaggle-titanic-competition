# Titanic Competition (Kaggle)

Solution to the Titanic competition on Kaggle.

## Table of Contents
* [Description](#description)
* [Dataset](#dataset)
* [Approach](#approach)
* [Technologies](#technologies)

## Description
The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew. While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, we're asked to build a predictive model that answers the question: **“what sorts of people were more likely to survive?”** using passenger data (ie name, age, gender, socio-economic class, etc).

## Dataset
We'll use **train.csv** for training our models and **test.csv** for testing out models. Specifically,
* **train.csv** contains the details of a subset of the passengers on board (891 to be exact) and the “ground truth”,
* **test.csv** dataset contains similar information but does not disclose the “ground truth” for each passenger.

You can find the dataset here: https://www.kaggle.com/c/titanic/data

## Approach
First, we explore the structure of the data by doing a simple exploratory analysis. <br/>
Following this analysis, we try to fix those examples that are missing values in certain features by making certain assumptions. For example, if a person's age is missing, we can fill this gap by taking the mean of the ages with repsect to a person's title (ex certain titles are given at a certain age). Also, we have changed the format of some feature values (ex create ranges by grouping values). <br/>
When this task is completed, we decide which features we're going to use and if possible we create new features that can give a better insight to our models. <br/>
Finally, we train our Machine Learning models and perform cross validation in order to evaluate our models and choose which of these models is going to be used for predictions. The evaluation metric that we use is **accuracy**. The current models in this project are:
* Logistic Regression,
* Decision Trees,
* Random Forest,
* Linear Support Vector Classifier.

## Technologies
The technologies used that are worth mentioning, are:
* Python,
* Pandas,
* scikit-learn.
