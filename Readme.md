# Module 20 Report Template

## Usage

* Run `Credit_Risk/credit_risk_classification.ipynb`

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

### Purpose of the analysis

The purpose of this analysis was to assess and compare machine learning models for predicting loan risk using historical data from a peer-to-peer lending platform. The objective was to develop a binary classification model that could determine if a loan applicant is high-risk or low-risk, in other words, to predict their creditworthiness.

### DataSet

The dataset contains the following features:
* loan_size: The size of the loan requested by the borrower.
* interest_rate: The interest rate assigned to the loan.
* borrower_income: The income of the borrower.
* debt_to_income: The borrower's debt-to-income ratio.
* num_of_accounts: The number of existing credit accounts.
* derogatory_marks: Number of negative marks (e.g., defaults or delinquencies) on the borrower's credit report.
* total_debt: Total outstanding debt.
* loan_status: The target variable, where:
* 0 = Low Risk (creditworthy)
* 1 = High Risk (not creditworthy)

### Target Variable Information (loan_status)

The target variable in this analysis is loan_status, which indicates the credit risk of a borrower:

* 0 = Low Risk (creditworthy)
* 1 = High Risk (not creditworthy)

**Value Counts:**

| loan_status | Count | Percentage |
| --- | --- | ---- |
| 0 |  75036 | 96.78% |
| 1 |  2500 | 3.22 % |

The class imbalance is evident, as the majority of borrowers are categorised as low-risk. The imbalance must be considered when evaluating model performance, particularly for metrics such as recall and precision for the minority class (1), which is composed of high-risk borrowers.

### Machine Learning Process

* Data Preparation : Dataset was loaded and cleaned using pandas
* Train-Test : The data was divided into training and testing sets with the help of train_test_split() from scikit-learn to ensure an unbiased evaluation.
* Model Selection : Due to its suitability for binary classification problems, like predicting credit risk, a Logistic Regression classifier was initially selected as the machine learning model.

## Results

* **Machine Learning Model 1: Logistic Regression**

  * **Accuracy**: 0.99
  * **Precision**:
    * Class 0 (Low Risk): 1.00
    * Class 1 (High Risk): 0.87
  * **Recall:**
    * Class 0 (Low Risk): 0.99
    * Class 1 (High Risk): 0.93
  * **F1-Score (High Risk)**: 0.90

## Summary

The logistic regression model performed exceptionally well in predicting loan risk, especially when taking into account the class imbalance in the dataset.

**Why this model is recommended?**

* The model's ability to detect the most risky applicants is demonstrated by its high recall (0.93) for high-risk borrowers.
* The model's high precision (0.87) for high-risk borrowers indicates that it is usually accurate when it predicts a borrower as high-risk.
* The accuracy of 99% further supports its strong performance, though it is not the sole metric considered due to class imbalance.
