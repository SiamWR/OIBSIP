# Iris Flower Classification

## Project Overview

This project builds a machine learning classification model to identify Iris flower species based on their physical measurements.

The model predicts three Iris species:

- Iris Setosa
- Iris Versicolor
- Iris Virginica

using the following measurements:

- Sepal length
- Sepal width
- Petal length
- Petal width


## Objective

The objective of this project is to train and compare classification models and select the best-performing model for Iris species prediction.


## Dataset

Dataset used:

Scikit-learn Iris Dataset

Source:

`sklearn.datasets.load_iris()`

Dataset details:

- 150 samples
- 4 numerical features
- 3 target classes


## Exploratory Data Analysis (EDA)

The following analyses were performed:

- Dataset shape inspection
- Data type checking
- Missing value analysis
- Descriptive statistics
- Pairplot visualization
- Feature distribution analysis using box plots

The analysis showed that petal length and petal width are the most discriminative features for separating Iris species.


## Machine Learning Models

The following classification models were trained:

1. Logistic Regression
2. K-Nearest Neighbors


## Model Evaluation

Models were evaluated using:

- Accuracy score
- Precision
- Recall
- F1-score
- Confusion Matrix


## Result

Logistic Regression was selected as the best-performing model based on higher validation accuracy while maintaining strong test performance.


## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
