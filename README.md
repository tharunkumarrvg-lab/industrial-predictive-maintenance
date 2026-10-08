# Industrial Predictive Maintenance with Machine Learning

> An explainable machine learning system for predicting industrial machine failures using sensor data, XGBoost, and SHAP.

## Overview

This project develops an end-to-end predictive maintenance pipeline to identify potential machine failures from industrial sensor measurements.

The workflow covers data cleaning, exploratory data analysis, feature engineering, machine learning, threshold optimization, model evaluation, and explainable AI.

## Business Problem

Unexpected equipment failures can cause production downtime, maintenance costs, and operational disruption.

**Objective:** Can machine operating conditions be used to predict machine failure before it occurs?

## Dataset

This project uses the **AI4I 2020 Predictive Maintenance Dataset** from the UCI Machine Learning Repository.

- 10,000 observations
- Industrial machine sensor measurements
- Binary machine-failure target
- Synthetic dataset designed to reflect industrial predictive-maintenance scenarios

**Dataset:** https://archive.ics.uci.edu/dataset/601/ai4i

> Note: This is public synthetic data and is not BMW, Siemens, or any company's proprietary data.

## Features

The project uses:

- Air temperature
- Process temperature
- Rotational speed
- Torque
- Tool wear
- Product type
- Temperature difference
- Mechanical power
- Tool wear level

Failure-mode indicators were excluded to reduce the risk of target leakage.

## Machine Learning Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Train/Test Split
   ↓
Logistic Regression Baseline
   ↓
XGBoost Classification
   ↓
Threshold Optimization

## Models

### Logistic Regression

Used as an interpretable baseline model for comparison.

### XGBoost

Used as the primary nonlinear classification model with class-imbalance handling.

## Evaluation

The project evaluates the model using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- Precision-Recall Curve

Recall is particularly important because missing an actual machine failure can result in unexpected downtime and maintenance costs.

## Threshold Optimization

Instead of relying only on the default `0.50` classification threshold, the XGBoost threshold was optimized using the precision-recall trade-off.

**Optimized threshold: 0.7423**

### Optimized Results

| Metric | Result |
|---|---:|
| Precision | 82.86% |
| Recall | 85.29% |
| F1 Score | 84.06% |

## Explainable AI

SHAP is used to interpret the XGBoost model and identify which sensor variables contribute most strongly to machine-failure predictions.

This improves model transparency and helps connect machine-learning predictions with potentially useful industrial insights.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook
- Git & GitHub

## Repository Structure

```text
industrial-predictive-maintenance/
├── README.md
├── Industrial_Predictive_Maintenance.ipynb
├── data/
├── results/
├── src/
├── requirements.txt
└── .gitignore
   ↓
Model Evaluation
   ↓
SHAP Explainability
Failure-mode indicators were excluded to reduce the risk of target leakage.

