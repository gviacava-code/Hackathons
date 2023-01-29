# Shinkansen Travel Experience

## 1. Problem Statement

The goal of the problem is to predict whether a passenger was satisfied or not considering his/her overall experience of traveling on the Shinkansen Bullet Train. This exercise also aims to determine the relative importance of each parameter with regards to their contribution to the passengers’ overall travel experience.

## 2. Data Description

The dataset contains a random sample of individuals who traveled on this train. Data is split in two different files: 1. The on-time performance of the trains along with passenger information. File Traveldata_train.csv’. 2. Passengers’ feedback on various parameters related to the travel along with their overall experience.  File ‘Surveydata_train.csv’.

* Number of observations  - 94379
* Number of variables/columns - 25 (6 numeric and 19 categorical )
* Variable Overall_Experience (categirucal - binary) is the target

## 3. Modelling Algorithms

Algorithms were selected following scikit-learn algorithm cheat-sheet flow chart for model selection

  * SVR (linear)
  * KNN
  * SVR (rbf)
  * Decision Tree
  * Random Forest
  * Voting Classifier

* Metrics - Since the target variable is a categorical variable, classification evaluation metrics accurracy_score, f1_socre, precision_socre and recall_score have been used.

## 4. Results

**Model Random Forest Classifier (rfc) perform as the best model** to work with this dataset. Performance metrics are:

* Train data set ->  Accuracy: 0.952   |   F1 score: 0.956    |    Precision: 0.963    |   Recall: 0.949
* Test data set  ->  Accuracy: 0.946   |   F1 score: 0.950    |    Precision: 0.955    |   Recall: 0.945
* Cross Validation Accuracy: Accuracy: 0.946 (+/- 0.001) [RandomForestClassifier]

This *Accuracy* factor shows the model is able to predict 95% of observations. A Precision and Recall of also 95, indicate this model is correctly classifying labels at a very high ratio.

![Summary Charts](https://github.com/giomvp/AcademicProjects/blob/40973c188cf5a2dbd5574e5ab54c995b0fd0fce3/ShinKansenTravelExperience/imgs/summary_plt.jpg)

Complete model selection analysis [here](https://github.com/giomvp/AcademicProjects/blob/767573a322a7e6cb785101cd4c0d3adba1f25e9e/ShinKansenTravelExperience/ShinkansenTravelExperience.ipynb).
