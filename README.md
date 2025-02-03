# 🚨 Canadian Anti-Fraud Centre Reporting Data Analysis 🚨

Welcome to the Canadian Anti-Fraud Centre Reporting Data Analysis project! This repository contains the analysis and machine learning models built to investigate fraud patterns using data from the Canadian Anti-Fraud Centre Fraud Reporting System. The dataset consists of 300,171 records and 21 features, detailing fraudulent activities reported across Canada. The primary goal is to uncover trends, identify the key factors contributing to fraud, and predict future fraudulent behavior.

## 📊 Project Overview

Fraud is a pressing issue impacting individuals, businesses, and governments worldwide. In Canada, fraudulent activities have escalated, prompting the need for data-driven solutions to detect and prevent these occurrences. This project aims to leverage data to predict fraud occurrences, uncover patterns, and support decision-making processes to reduce fraudulent activities.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Predictive Models](#predictive-models)
- [Results and Evaluation](#results-and-evaluation)
- [How to Run the Code](#how-to-run-the-code)


## 📑 Data Description

The dataset consists of 300,171 fraud reports with 21 features. The key features include:

- **Fraud Type**: Category of fraud (e.g., identity theft, payment fraud)
- **Date Reported**: Date of the fraud report
- **Location**: Geographic location of the fraud incident
- **Victim Profile**: Demographic information of the victim
- **Dollar Loss**: The financial loss caused by the fraud

## 🧹 Data Preparation

The dataset underwent extensive data cleaning and preprocessing to ensure its quality:

- **Missing Values**: Missing data in demographic and location columns were imputed or removed.
- **Duplicate Entries**: Duplicates were removed to prevent skewing the results.
- **Z-Score Normalization**: Financial loss data was normalized using the Z-score method, and 1,100 outliers were identified for further consideration.
- **Feature Engineering**: Additional time-based features like 'Year' and 'Month' were created from the `Date Reported` field.
- **Data Type Conversion**: Columns were converted to appropriate data types (e.g., date fields to datetime, categorical fields to factors).

## 📊 Exploratory Data Analysis (EDA)

Various data visualizations were created to explore trends and patterns in the fraud data:

- **📈 Complaints Over Time**: Line chart showing trends and spikes in fraud reports.
- **🏙️ Top 10 Provinces with Fraud Reports**: Bar chart highlighting regions with high fraud activity.
- **📞 Top 5 Solicitation Methods**: Bar chart illustrating the most common methods of solicitation used by fraudsters.
- **💸 Financial Loss Distribution**: Pie chart depicting the percentage of fraud complaints resulting in financial loss.

## 🤖 Predictive Models

Several machine learning models were developed to predict and classify fraud occurrences:

1. **Logistic Regression**: Used to classify fraud reports, improved with LASSO regularization to boost model accuracy.
2. **Random Forest**: Ensemble learning method to capture complex interactions and predict fraud reports.
3. **XGBoost**: High-performance model used to predict financial loss from fraud reports.
4. **Time Series Model**: ARIMA model used to forecast the number of fraud complaints over time.
5. **Random Forest with PCA**: Used Principal Component Analysis (PCA) to reduce dimensionality, improving computational efficiency.

### 🏆 Results and Evaluation

- **Logistic Regression**: Achieved an accuracy of 93% after applying LASSO regularization.
- **Random Forest**: Accuracy of 95%, with precision around 94% and recall close to 96%.
- **XGBoost**: High performance in predicting financial loss, with excellent metrics in precision, recall, and F1 score.
- **Time Series Model**: The ARIMA model forecasted the number of complaints with a Mean Absolute Percentage Error (MAPE) of 33.96%.
- **Random Forest with PCA**: Achieved an accuracy of 83%, with improved interpretability and reduced training time.

## 🚀 How to Run the Code

### 🔧 Prerequisites

Make sure you have the following libraries installed:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`
- `statsmodels`

