# Credit Card Delinquency Classification

This repository contains an end-to-end project for analyzing and predicting credit card payment delinquency using advanced machine learning techniques. The workflow includes performing Exploratory Data Analysis (EDA), extensive feature engineering, training and comparing multiple classifiers, hyperparameter optimization with Optuna, model explainability with SHAP, and an interactive dashboard built with Dash for data visualization and exploration.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [EDA & Feature Engineering](#eda--feature-engineering)
- [Modeling](#modeling)
- [Hyperparameter Optimization](#hyperparameter-optimization)
- [Model Explainability](#model-explainability)
- [Interactive Dashboard](#interactive-dashboard)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [File Structure](#file-structure)
- [License](#license)

## Project Overview

The project solves the problem of predicting the probability of credit card clients defaulting on their next payment. The dataset used is the "default of credit card clients" dataset, with a workflow including:
- Data loading and cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering (binned age, delay and payment features, utilization ratios, OHE for categoricals, etc.)
- Model training and evaluation (Logistic Regression, Random Forest, Decision Tree, XGBoost, LightGBM)
- Hyperparameter tuning with Optuna
- ROC and metrics visualization
- SHAP-based model explanation
- Interactive dashboard for exploring data and model results

## Features

- **EDA:** Distributions by demographic and financial features, delay and repayment profiles.
- **Feature Engineering:** Creation of payment behavior metrics, categorical encoding, utilization calculation, payment/bill trends.
- **ML Modeling:** Baseline and advanced classifiers, including hyperparameter-tuned LightGBM.
- **Optuna Integration:** Automated hyperparameter optimization for best ROC-AUC.
- **Model Explanation:** Visualization of feature importances with SHAP.
- **Interactive Dashboard:** Dash app for exploring data, feature distributions, and summary statistics.

## Dataset

- **Source:** "Default of Credit Card Clients" dataset ([UCI link, not included here])
- **File:** `default of credit card clients.xlsx`
- **Features:** Demographic, financial, payment history, bill amount, and payment amount for 30,000 clients

## EDA & Feature Engineering

- Mapped and cleaned categorical variables (Sex, Marriage, Education)
- Binned ages
- Created statistical features: average/max delay, number of delayed months, repayment ratio, trends, and utilization features
- One-hot encoding for categorical columns
- Prepared train-test splits and scaling for modeling

## Modeling

- **Models compared:** 
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
- **Evaluation:** ROC AUC score, classification report, ROC curve visualization

## Hyperparameter Optimization

- **Optuna + LightGBM:** 
  - 50 trials of hyperparameter search
  - 5-fold stratified cross-validation
  - Best parameters saved and used for final model
- **Metrics:** Reporting best ROC-AUC and classification on the holdout set

## Model Explainability

- **SHAP:** Global and local explainability of the final LightGBM model; feature importance plots included.

## Interactive Dashboard

- Built in Dash (Plotly).
- Interactive selection and visualization of any feature.
- Compares distributions against default status.
- Summarizes value counts and displays sample data.

### Running the Dashboard

1. Install requirements:
