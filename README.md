# Insurance Claim Severity Prediction

## Project Overview

Insurance companies face significant financial risk from inaccurate claim estimation. Predicting claim severity helps insurers improve premium pricing, risk assessment, underwriting decisions, and profitability.

This project focuses on predicting insurance claim severity using customer demographics, vehicle characteristics, driving history, and policy information. The analysis includes extensive exploratory data analysis, feature engineering, multicollinearity assessment, machine learning model development, hyperparameter tuning, and model explainability.

---

## Business Problem

Insurance providers need to accurately estimate future claim amounts in order to:

- Price policies appropriately
- Identify high-risk policyholders
- Reduce financial losses
- Improve underwriting decisions
- Optimize risk management strategies

The objective of this project is to predict insurance claim severity (Claim Amount) using historical policyholder and vehicle data.

---

## Dataset Information

The dataset contains over 10,000 insurance records with customer, vehicle, and claim-related attributes.

### Key Feature Categories

#### Customer Information
- Age
- Gender
- Education
- Occupation
- Marital Status
- Income

#### Vehicle Information
- Car Type
- Vehicle Value (Bluebook)
- Vehicle Age
- Commercial/Private Usage

#### Driving History
- Motor Vehicle Record Points
- Previous Claims
- Claim Frequency
- License Revocation Status

#### Policy Information
- Time In Force (TIF)
- Home Value
- Urbanicity

### Target Variable

- `CLM_AMT` (Claim Amount)

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- SHAP
- Jupyter Notebook

---

## Project Workflow

### 1. Data Cleaning & Preprocessing

- Missing value treatment
- Data type conversion
- Currency field transformation
- Median imputation
- Outlier handling
- Winsorization
- Log transformations

### 2. Exploratory Data Analysis (EDA)

Performed:

- Univariate Analysis
- Bivariate Analysis
- Correlation Analysis
- Distribution Analysis
- Customer Segmentation
- Risk Profiling

Visualizations include:

- Histograms
- Boxplots
- Correlation Heatmaps
- Pairplots
- Violin Plots
- Scatter Plots

---

## Feature Engineering

Several business-driven features were created to improve model performance.

### Risk Features

- Claim Rate
- Risk Score
- Claim-to-Income Ratio
- Claim-to-Car-Age Ratio
- Severity Ratio

### Customer Features

- Driving Experience
- Generation Group
- Job Stability Index
- Career Gap Indicator
- Family Risk Score

### Vehicle Features

- Old Car Indicator
- Risky Vehicle Indicator

### Business Features

- Urban Wealth Indicator
- Policy Lifetime Value
- Claim Acceleration Rate
- Urban Risk Multiplier

---

## Multicollinearity Analysis

Variance Inflation Factor (VIF) was used to detect multicollinearity among predictors.

### Actions Taken

- Identified highly correlated variables
- Removed redundant features
- Recalculated VIF scores
- Retained statistically meaningful variables

---

## Machine Learning Models

### Random Forest Regressor

Used for:

- Baseline prediction
- Feature importance analysis
- Hyperparameter optimization

### Hyperparameter Tuning

Performed using:

- RandomizedSearchCV

Optimized parameters:

- Number of Trees
- Maximum Depth
- Minimum Samples Split
- Minimum Samples Leaf

### XGBoost Regressor

Built to compare performance against Random Forest and improve predictive accuracy.

---

## Model Evaluation Metrics

The following metrics were used:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score
- 5-Fold Cross Validation

---

## Model Results

### Random Forest Regressor

#### Before Tuning

- R² (Train): 0.9905
- R² (Test): 0.9786

#### After Tuning

- R² (Train): 0.9322
- R² (Test): 0.9529

### XGBoost Regressor

- R² (Train): 0.9979
- R² (Test): 0.9565

The models demonstrated strong predictive performance while maintaining good generalization on unseen data.

---

## Model Explainability

SHAP (SHapley Additive Explanations) was used to understand feature contributions.

### Most Important Features

- Claim-to-Income Ratio
- Income
- Home Value
- Vehicle Value (Bluebook)
- Previous Claims
- Claim Age Ratio

---

## Key Business Insights

### Customer Risk

- Lower-income customers tend to have higher claim severity.
- Commercial vehicle users generally generate larger claims.
- Urban customers exhibit higher claim risk than rural customers.

### Vehicle Risk

- SUVs and Sports Cars show higher claim severity.
- Older vehicles tend to generate more expensive claims.

### Demographic Insights

- Middle-aged customers represent the highest-risk segment.
- Education level shows an inverse relationship with claim amount.

### Pricing Recommendations

- Adjust premiums based on vehicle type and usage.
- Implement risk-based pricing using customer income and driving history.
- Introduce differentiated pricing for urban and commercial vehicle owners.

---

## Business Impact

This solution can help insurance companies:

- Improve underwriting decisions
- Optimize premium pricing
- Detect high-risk policyholders
- Reduce financial losses
- Improve profitability
- Support data-driven risk management

---

## Repository Structure

```text
insurance-claim-severity-prediction/
│
├── data/
│   └── insurance_claims.csv
│
├── notebooks/
│   └── insurance_claim_severity_prediction.ipynb
│
├── reports/
│   └── Insurance_Claim_Severity_Prediction_Report.pdf
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

## Future Improvements

- Streamlit Deployment
- Insurance Risk Dashboard
- Ensemble Modeling
- Automated Premium Recommendation System
- Real-Time Claim Prediction API

---

## Author

**Anuj Oraon**

Aspiring Data Analyst passionate about solving business problems using data analytics, statistics, machine learning, and visualization.# insurance-claim-severity-prediction
