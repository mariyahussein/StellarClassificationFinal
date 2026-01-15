# Stellar Classification – Capstone Project

This repository contains the final capstone project for classifying stars into different star types based on their physical properties. The goal of the project is to explore the dataset through EDA and build machine learning models capable of predicting a star's type using measurements such as temperature, luminosity, radius, and spectral class.

## Project Goal

The main objective is to compare different classification models and evaluate how well they can distinguish between star types using supervised learning. This includes a baseline model and at least one additional model for comparison.

## Dataset

The dataset is sourced from Kaggle:

https://www.kaggle.com/datasets/deepu1109/star-dataset

The dataset consists of 240 stars and includes the following features:

- Temperature (K)
- Luminosity (L/Lo)
- Radius (R/Ro)
- Absolute Magnitude (Mv)
- Star Color
- Spectral Class
- Star Type (target column with classes 0–5)

No missing values or duplicate rows were found, so no major cleaning was required.

## Methods

The project is divided into three main parts:

### 1. Exploratory Data Analysis (EDA)
EDA was performed to better understand the dataset. This included:
- Summary statistics
- Checking data types
- Visualizing distributions of numerical features
- Counting categorical feature values
- Plotting temperature vs luminosity (HR-style diagram)
- Examining class distribution for target variable

### 2. Data Preprocessing
Before modeling, the following steps were completed:
- One-hot encoding of categorical variables (Star Color, Spectral Class)
- Train/test split with stratification (80/20)
- Feature scaling for KNN using StandardScaler
- Numerical features were left unscaled for tree-based models

### 3. Machine Learning Models
Three supervised classification models were trained and tested:
- Decision Tree Classifier (baseline)
- K-Nearest Neighbors (KNN) Classifier (comparison model)
- Random Forest Classifier (additional model)

Performance was evaluated using accuracy and classification reports on the test set.

## Results

Model performance on the held-out test set:

- Decision Tree: achieved perfect accuracy on this dataset
- KNN: performed well but lower than the tree-based models
- Random Forest: achieved very high accuracy 


These results suggest that tree-based models are well-suited for this dataset and that the physical properties of stars are strong predictors for star classification.

