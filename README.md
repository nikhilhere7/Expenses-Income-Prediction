                                                                        Income & Expense Prediction Using Machine Learning

Predicting customer income & expenses using transaction data
Tech Stack: Python · Pandas · Scikit-Learn · Random Forest · Matplotlib · Seaborn

Project Overview

This project analyzes Bank transaction data and builds machine learning models to predict:

Total income per customer
Total expenses per customer

The dataset contains detailed customer transactions 
The goal is to use these raw transactions to understand customer behavior and build predictive models using feature engineering and regression algorithms.

Project Structure
Expenses-Income-Prediction/
│── README.md
│── requirements.txt
│── data/
│   └── anz_cleaned.csv
│── models/
│   ├── best_income_model.pkl
│   └── best_expense_model.pkl
│── images/
│   ├── predicted_vs_actual_income.png
│   ├── predicted_vs_actual_expense.png
│   ├── feature_importance_income.png
│   └── feature_importance_expense.png
│── notebooks/
│   ├── 01_data_prep.ipynb
│   ├── 02_features_models.ipynb
│   └── 03_evaluation.ipynb
│── report/
│   └── final_report.pdf

Dataset Description

customer_id – unique user
movement – credit (income) or debit (expense)
amount – transaction value
txn_description – transaction category
balance – account balance
date – timestamp
merchant details, locations, gender, age, etc.

Targets created:

total_income = sum of all credit amounts
total_expenses = sum of all debit amounts

Feature Engineering

Created features include:

Feature				Description
total_transactions	Total number of transactions
debit_count		Number of debit txns
credit_count		Number of credit txns
avg_amount		Avg. transaction amount
max_amount		Maximum amount spent
min_amount		Minimum amount spent

Machine Learning Models

Two models were trained:

Linear Regression
Baseline for comparison.

Random Forest Regressor
Final model used for prediction.

Models were trained separately for:

Income
Expenses

Train/test split = 80/20
