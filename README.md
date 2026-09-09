# Diabetic Foot Ulcer Prediction Using Machine Learning and SHAP

## Project Overview

This project presents a machine learning framework for predicting
Diabetic Foot Ulcer (DFU) status using clinical, biochemical,
hormonal, and lifestyle-related variables.

## Objective

The objective was to develop and evaluate machine learning models
for binary classification of DFU status and interpret important
predictors using SHAP analysis.

## Dataset

The study included 550 patients with diabetes:

- 397 DFU-positive cases
- 153 DFU-negative cases

The original hospital dataset is not publicly included because
of privacy and confidentiality considerations.

## Models

Three machine learning models were evaluated:

- Random Forest
- XGBoost
- Support Vector Machine

## Evaluation

Models were evaluated using:

- Accuracy
- Sensitivity
- Specificity
- Precision
- F1-score
- ROC-AUC

## Explainability

SHAP analysis was used to investigate the contribution of predictors
to model predictions.

## Tools

- R
- Random Forest
- XGBoost
- SVM
- SHAP
- ggplot2
- caret
- pROC
- fastshap

## Key Findings

Random Forest demonstrated strong predictive performance on the
study dataset, achieving 96.3% accuracy and an ROC-AUC of 0.990.

## Disclaimer

This project represents an academic research analysis and is not
intended to serve as a clinical diagnostic tool.
