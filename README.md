# Loan Eligibility Prediction – Project Summary

This project focuses on predicting whether a loan application should be approved or rejected, based on a set of financial indicators such as:

- CIBIL score
- Annual income (`income_annum`)
- Loan amount
- Loan term (assumed to be in months)

## Goal

To build and evaluate machine learning models that can generalize well and make realistic decisions based on the input data, including both typical and extreme cases.

## Data Preparation

- The dataset did not specify currency or units, so for the purpose of this project:
  - Loan term is assumed to be in **months**
  - Income and loan amount values were divided by **100** for interpretability (they appeared to be stored as floats with `.00`)
- All categorical variables were converted to numeric
- Additional **extreme test cases** were generated to improve the model's ability to handle edge scenarios (e.g., high CIBIL + low income)

## Models Used

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

## Evaluation Strategy

- Classification reports (Accuracy, Precision, Recall, F1-score)
- Probability-based interpretation with `predict_proba()`
- Case-based testing with realistic and unrealistic combinations
- Feature importance analysis

## Key Insights

- CIBIL score was the most influential feature, but not the only one
- Adding synthetic edge cases improved generalization
- Models sometimes approved risky applications if the CIBIL score was high
- XGBoost offered the most consistent and explainable performance

## Technologies

- Python 3.10+
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost
- JupyterLab

## How to run
1. Clone the repository and install dependencies:

```bash
git clone https://github.com/jacek-kozakowski/loan-eligibility-prediction.git
cd loan-eligibility-prediction
pip install -r requirements.txt
```

2. Navigate to project directory and open the notebook:

```bash
jupyter lab LoanEligibilityPrediction.ipynb
```
---

## 👤 Author

**Jacek Kozakowski** – [LinkedIn](https://www.linkedin.com/in/jacek-kozakowski-31b759356/)

---
