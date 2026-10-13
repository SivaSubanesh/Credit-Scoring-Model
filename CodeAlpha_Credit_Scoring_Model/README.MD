📊 Credit Scoring Model (Loan Default Prediction)
📌 Project Overview

This project focuses on building a Credit Scoring Model to predict whether a loan applicant is likely to default based on financial and credit-related features.
The model is trained and evaluated using multiple machine learning algorithms and compares their performance.

The goal is to assist financial institutions in risk assessment and loan approval decisions.

📁 Dataset

The dataset is downloaded directly from Google Drive using gdown.

Features:

income – Applicant’s annual income

loan_amount – Loan amount requested

term – Loan tenure (36 or 60 months)

credit_history – Credit history availability (0 or 1)

defaulted – Target variable (0 = No default, 1 = Default)

Dataset Shape:

Rows: 1248  
Columns: 5

🔧 Tools & Libraries Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

🧹 Data Preprocessing
1. Handling Missing Values

income → filled using median

loan_amount → filled using median

credit_history → filled using mode

2. Feature Engineering

Created a binary feature:

term_binary = 1 if term == 60 else 0


Applied log transformation on:

income

loan_amount

Standardized features using StandardScaler

📊 Exploratory Data Analysis (EDA)

The following visualizations were created:

Income distribution

Loan amount distribution

Loan term distribution

Credit history vs loan default

Correlation heatmap

These insights helped understand feature relationships and default patterns.

🧠 Machine Learning Models

The following models were trained and evaluated:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Train-Test Split:

80% Training

20% Testing

Stratified on target variable

📈 Model Performance
Logistic Regression

Accuracy: ~66%

Good precision for non-default cases

Lower recall for defaulted loans

Decision Tree

Accuracy: ~57%

Moderate performance with some overfitting

Random Forest

Accuracy: ~62%

More balanced performance than Decision Tree

📌 Best Model: Logistic Regression (based on overall stability and accuracy)