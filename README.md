# MIMIC-IV AKI Prediction

Predicting **Acute Kidney Injury (AKI)** in ICU patients using clinical data from the MIMIC-IV database and machine learning techniques.

## Overview

Acute Kidney Injury (AKI) is a serious condition associated with increased mortality, prolonged hospital stays, and higher healthcare costs. Early identification of patients at risk can enable timely intervention and improve outcomes.

This project develops machine learning models to predict AKI using patient demographics, laboratory measurements, physiological variables, and clinical scores extracted from the **MIMIC-IV** critical care database.

## Objectives

* Build a predictive pipeline for AKI detection.
* Engineer clinically meaningful features from ICU data.
* Compare multiple machine learning models.
* Evaluate model performance using standard classification metrics.
* Interpret model predictions using SHAP explainability.

## Dataset

The project uses data derived from the **MIMIC-IV (Medical Information Mart for Intensive Care)** database, a large publicly available dataset containing de-identified health records from ICU patients.

### Features Used

Examples of extracted features include:

* Age
* Weight
* Creatinine levels
* Blood Urea Nitrogen (BUN)
* Chloride levels
* Urine Output
* Fluid Balance
* Glasgow Coma Scale (GCS)
* SOFA Score
* Admission Type

## Methodology

### 1. Data Extraction

Clinical data were extracted from MIMIC-IV using SQL queries and BigQuery.

### 2. AKI Label Generation

AKI labels were created using kidney-function-related measurements and clinical criteria.

### 3. Feature Engineering

Additional features were generated from:

* Laboratory values
* Urine output trends
* Clinical severity scores
* Temporal measurements

### 4. Model Development

The following models were evaluated:

* Logistic Regression
* Random Forest
* XGBoost
* Ensemble Models

### 5. Explainability

SHAP (SHapley Additive exPlanations) was used to identify the most influential features contributing to model predictions.

## Results

Key observations:

* XGBoost achieved the strongest predictive performance.
* Kidney-function-related features were among the most important predictors.
* SHAP analysis provided clinically interpretable explanations for model decisions.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* SHAP
* Matplotlib
* Google BigQuery

## Repository Structure

```text
.
├── AKI_Prediction_MIMIC_IV.ipynb
├── README.md
├── requirements.txt
└── report.pdf
```

## Installation

```bash
pip install -r requirements.txt
```

## Running the Project

Open the notebook:

```bash
jupyter notebook AKI_Prediction_MIMIC_IV.ipynb
```

or run it using Google Colab.

## Future Improvements

* Incorporate temporal deep learning models (LSTM/Transformer).
* Perform hyperparameter optimization.
* Add external validation datasets.
* Explore real-time AKI risk prediction in ICU settings.

## Author

**Janhavi**

