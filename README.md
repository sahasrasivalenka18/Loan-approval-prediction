# Loan Approval Prediction

A machine learning project that predicts whether a loan application is likely to be approved based on selected applicant and loan-related features.

## Project Overview

The project uses a loan approval dataset and builds classification models to predict `Loan_Status`.

The workflow includes:

1. Loading the loan dataset
2. Inspecting the dataset and target distribution
3. Converting loan status (`Y` / `N`) into binary values
4. Selecting relevant features
5. Removing rows with missing values
6. Splitting the data into training and testing sets
7. Training a Logistic Regression model
8. Evaluating the model
9. Inspecting Logistic Regression coefficients
10. Training a Decision Tree classifier
11. Inspecting tree depth, number of leaves, and feature importance
12. Generating predictions for a separate test dataset

## Features

The models use the following features:

- `ApplicantIncome`
- `CoapplicantIncome`
- `LoanAmount`
- `Credit_History`

Target:

- `Loan_Status`

Where:
- `Y` = Loan approved
- `N` = Loan not approved

## Models

### Logistic Regression

The notebook trains a Logistic Regression classifier and evaluates it using accuracy.

The original notebook produced an accuracy of **84.40%** on its 20% test split after removing missing values.

### Decision Tree

A Decision Tree classifier is also trained. The notebook examines:

- Tree depth
- Number of leaves
- Feature importance

In the original run, the tree had a depth of **14** and **106 leaves**.

## Dataset Processing

The original dataset contains **614 rows and 13 columns**.

After selecting the four model features and `Loan_Status`, rows containing missing values were removed, leaving **543 rows** for modeling.

The data was split into:

- Training set: 434 rows
- Testing set: 109 rows

## Prediction Output

The notebook also accepts a separate test CSV and generates:

`loan_approval_predictions.csv`

The output contains:

- `Loan_ID`
- `Predicted_Loan_Status`

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Google Colab

## How to Run

1. Open `loan_approval_prediction.ipynb` in Google Colab.
2. Upload the training CSV when prompted.
3. Run the notebook cells in order.
4. Upload the test CSV when prompted for predictions.
5. The notebook generates `loan_approval_predictions.csv`.

## Project Structure

```text
loan-approval-prediction/
│
├── loan_approval_prediction.ipynb
├── README.md
└── requirements.txt
```

## Future Improvements

- Handle missing values using imputation instead of dropping rows.
- Compare additional classification algorithms.
- Add precision, recall, F1-score, and confusion matrix.
- Tune model hyperparameters.
- Add visualizations for exploratory data analysis.
- Build a simple web interface for making individual loan predictions.
