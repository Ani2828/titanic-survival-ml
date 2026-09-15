# Titanic Survival Prediction

A machine learning classification project that predicts whether a passenger survived the Titanic disaster using Python, Pandas, and Scikit-learn.

## Project Overview

The goal of this project is to build a binary classification model that predicts passenger survival based on passenger information.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Seaborn
- Matplotlib
- Google Colab

## Machine Learning Workflow

1. Loaded the Titanic dataset
2. Explored the dataset and identified missing values
3. Selected relevant features
4. Split the data into training and testing sets
5. Handled missing numerical and categorical values
6. Applied one-hot encoding to categorical variables
7. Built a Scikit-learn preprocessing pipeline
8. Trained a Logistic Regression classifier
9. Evaluated the model using accuracy, F1 score, and a confusion matrix

## Features Used

The model uses:

- Passenger class (`pclass`)
- Sex (`sex`)
- Age (`age`)
- Number of siblings/spouses (`sibsp`)
- Number of parents/children (`parch`)
- Fare (`fare`)
- Port of embarkation (`embarked`)

## Model

**Logistic Regression**

The model was implemented using a Scikit-learn Pipeline with a ColumnTransformer to ensure preprocessing was fitted only on the training data.

## Results

| Metric | Score |
|---|---:|
| Test Accuracy | **80.45%** |
| F1 Score | **72.44%** |

## Confusion Matrix

```text
                    Predicted
                  Did Not   Survived
                  Survive

Actual Did Not      98        12
       Survive      23        46
