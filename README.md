# Diabetic Foot Ulcer Prediction Using Machine Learning and SHAP

## Project Overview

This project presents a machine learning approach for predicting Diabetic Foot Ulcer (DFU) status using clinical and metabolic patient data. The analysis was developed as part of an M.Phil. Statistics research project and focuses on predictive modelling, model evaluation, feature importance, and model explainability.

Three machine learning classification methods were evaluated:

- Random Forest (RF)
- XGBoost
- Support Vector Machine (SVM)

SHAP (SHapley Additive exPlanations) was used to improve the interpretability of the machine learning results and identify variables that contributed most to the model predictions.

## Dataset

The study dataset contains **550 observations** and **31 predictor variables**, with DFU status as the binary outcome.

DFU distribution:

- Positive: 397 (72.2%)
- Negative: 153 (27.8%)

The predictors include demographic, clinical, metabolic, hormonal, lipid, liver, and kidney-related variables such as age, BMI, WHR, ABI, HbA1c, fasting blood glucose, testosterone, triglycerides, cholesterol, creatinine, eGFR, and UACR.

### Data privacy

The original dataset contains hospital/patient research data and is **not included in this repository**. The repository contains analysis scripts, figures, and selected results rather than the original patient-level dataset.

## Methods

The project follows these main stages:

1. Data preparation and inspection
2. Training of machine learning classification models
3. Model performance evaluation
4. Comparison of model performance
5. Feature-importance analysis
6. SHAP-based model explainability
7. Visualization and interpretation of results

The main model comparison uses a train/test approach, with the modelling workflow implemented in R.

## Models

### Random Forest

Random Forest was used as a tree-based ensemble classification method capable of modelling nonlinear relationships and interactions among predictors.

### XGBoost

XGBoost was used as a gradient-boosting classification method. It builds an ensemble of decision trees sequentially and is effective for complex nonlinear patterns.

### Support Vector Machine

SVM was included as a different machine learning approach for binary classification. Its feature-importance analysis was based on the magnitude of the model weights.

## Model Evaluation

The models were evaluated using:

- Accuracy
- Sensitivity (Recall)
- Specificity
- Precision
- F1-score
- ROC-AUC

The thesis analysis reported strong predictive performance for the tree-based models. Random Forest achieved approximately **96.3% accuracy** and an **ROC-AUC of 0.990** on the reported test results.

The detailed evaluation outputs and figures are provided in the `results` and `figures` folders.

## Feature Importance and Explainability

Different approaches were used to examine influential predictors:

- Random Forest: Gini-based feature importance
- XGBoost: gain-based feature importance
- SVM: absolute model weights
- SHAP: mean absolute SHAP values

SHAP was included because traditional feature-importance measures show which variables are influential, while SHAP provides an interpretable framework for examining how predictor variables contribute to model predictions.

## Repository Structure

```text
diabetic-foot-ulcer-prediction/
│
├── R/
│   ├── 01_data_preparation.R
│   ├── 02_model_training.R
│   ├── 03_model_evaluation.R
│   ├── 04_feature_importance.R
│   └── 05_shap_analysis.R
│
├── figures/
│   ├── dfu_distribution/
│   ├── model_performance/
│   ├── radar_plots/
│   ├── feature_importance/
│   ├── roc_auc/
│   └── shap/
│
├── results/
│   └── model_performance.csv
│
├── README.md
└── .gitignore
```

## Main Scripts

| Script | Purpose |
|---|---|
| `01_data_preparation.R` | Data loading, inspection, and preparation |
| `02_model_training.R` | Training the RF, XGBoost, and SVM models |
| `03_model_evaluation.R` | Calculating and comparing model performance metrics |
| `04_feature_importance.R` | Examining model-specific feature importance |
| `05_shap_analysis.R` | Performing SHAP-based model explainability |

## Figures

The `figures` directory is organized into separate folders for easier navigation:

- `dfu_distribution/` — DFU outcome distribution
- `model_performance/` — model performance comparisons
- `radar_plots/` — model performance radar plots
- `feature_importance/` — RF, XGBoost, and SVM feature-importance plots
- `roc_auc/` — ROC curve and AUC comparison
- `shap/` — SHAP importance visualization

## Key Findings

The analysis showed that machine learning methods can provide strong predictive performance for DFU classification using the available clinical and metabolic variables.

Random Forest and XGBoost demonstrated higher overall classification performance than SVM in the reported analysis. Feature-importance and SHAP analyses also highlighted the relevance of several metabolic, hormonal, and clinical variables.

These findings are intended for **academic and research purposes** and should not be interpreted as a clinical diagnostic system.

## Tools and Technologies

- **R**
- Random Forest
- XGBoost
- Support Vector Machine
- SHAP / `fastshap`
- `caret`
- `ggplot2`
- `pROC`
- `readxl`
- `dplyr`

## Research Context

This repository accompanies an M.Phil. Statistics research project titled:

**“Modeling Diabetic Foot Using Machine Learning Techniques”**

The project demonstrates the application of statistical and machine learning techniques to a healthcare prediction problem, with emphasis on model comparison and interpretability.

## Author

**Iman Fatima**

M.Phil. Statistics

GitHub: `Imanfatimah`

LinkedIn: `linkedin.com/in/imanfatima1999`

## Note

The repository is intended to demonstrate the analytical workflow and research methodology. Patient-level hospital data are not publicly shared.
