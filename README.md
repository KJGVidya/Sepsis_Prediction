
# Sespis Prediction Using ML

Predicting sepsis in hospital patients 6 hours before onset of sepsis.

## Introduction
Sepsis is the body’s extreme response to an infection. It is a life-threatening medical emergency.  Sepsis happens when an infection you already have triggers a chain reaction throughout your body.  Infections that lead to sepsis most often start in the lung, urinary tract, skin, or gastrointestinal tract. Without timely treatment, sepsis can rapidly lead to tissue damage, organ failure, and death.


## Project Goal
Early detection of sepsis i.e., 6 hours ahead of onset of sepsis using hourly time series data. We are provided with patients' vital signs, laboratory values and demographics.

Build a model which could pick up trends and predict sepsis with high recall.


## Dataset
For this study, we use clinical data of ICU patients from two separate hospital systems provided by UCI Machine Learning Repository.

Patient: ~40K. 
Sepsis Patient:~3K

SepsisLabel is set to 1, six hours before the onset of sepsis aiding in early prediction. For non-sepsis patients, SepsisLabel is 0.


## Models
A large portion of the data is missing. Missing values are imputed using Backward and forward fill, and MICE.

**Imputation method**
* Backward and Forward fill.
* MICE (Multiple Imputation using Chained Equations)

**Classification Models**
* XGBoost (Xtreme gradient Boosting)
* LightGBM (Light Gradient Boosting Machine)

## NoteBooks
We use Jupyter NoteBooks to explore and model the dataset.

* EDA - 01 Sepsis Analysis.ipynb
* Data Preprocessing 02 - Missing values and Outliers.ipynb
* Data Preprocessing - 03 - Feature Engineering and Selection.ipynb
* Training Models - 04 - XGboost and LightGBM.ipynb


## Evaluating Models

In Sepsis prediction, recall is important than accuracy. Recall/sensitivity is how many of actual sepsis records were predicted correctly.

We use Precision-Recall curve to evaluate our model.

XGBoost PR Curve           |  LightGBM PR Curve
:-------------------------:|:-------------------------:
![](https://github.com/KJGVidya/Sepsis_Prediction/blob/main/Images/XGBoost%20PR%20Curve%20Mean.png)  |  ![](https://github.com/KJGVidya/Sepsis_Prediction/blob/main/Images/LightGBM%20PR%20Curve%20mean.png)
