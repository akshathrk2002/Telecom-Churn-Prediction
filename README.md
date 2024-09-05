# Telecom Customer Churn Prediction using XGBoost

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Data Preprocessing](#data-preprocessing)
5. [Model Training](#model-training)
6. [Model Evaluation](#model-evaluation)
7. [Installation](#installation)
8. [Usage](#usage)

## Project Overview
This project aims to predict customer churn in the telecom industry using a machine learning approach. We employed an XGBoost Classifier to analyze customer behavior data and identify patterns that may indicate whether a customer is likely to churn.

## Features
- Predicts customer churn based on telecom customer data.
- Data preprocessing includes handling missing values, encoding categorical data, and normalizing features.
- Detailed evaluation using metrics like accuracy, ROC-AUC, and classification report.

## Technologies Used
- **Programming Language:** Python
- **Libraries:** XGBoost, Pandas, NumPy, Scikit-learn
- **Machine Learning Model:** XGBoost Classifier

## Data Preprocessing
The dataset used includes both numerical and categorical data. Key preprocessing steps:
- Converted categorical variables like `gender`, `Partner`, and `Dependents` into binary values.
- Transformed multi-class features such as `InternetService` and `Contract` into numerical equivalents.
- Handled missing or erroneous data in the `TotalCharges` column by replacing empty entries with `0` and converting the column to a numeric data type.

## Model Training
We trained the XGBoost model with the following parameters:
- `n_estimators=100`
- `max_depth=3`
- `learning_rate=0.1`
Data was split into training and test sets using an 80/20 split.

## Model Evaluation
The model was evaluated using several performance metrics:
- **Accuracy:** The model’s accuracy in predicting customer churn.
- **ROC-AUC:** A measure of how well the model distinguishes between churn and non-churn customers.
- **Classification Report:** Provided detailed precision, recall, and F1-score for both classes (churn, no churn).

## Installation
To run the project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Place your dataset in the root directory of the project.
2. Run the script to preprocess the data, train the model, and evaluate the results:
    ```bash
    python churn_prediction.py
    ```
