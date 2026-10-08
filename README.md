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
   ↓
Model Evaluation
   ↓
SHAP Explainability
Failure-mode indicators were excluded to reduce the risk of target leakage.

