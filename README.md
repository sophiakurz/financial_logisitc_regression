# Logistic Regression in Financial Data

## Overview
This project involves the implementation of logistic regression for binary classification in a financial context. The primary aim is to identify fraudulent transactions within a financial dataset. Logistic regression, a fundamental machine learning technique, is used here due to its effectiveness in binary classification problems.

## Dataset
The dataset, named `financial.csv`, consists of financial transactions with features relevant for detecting fraud. Key features include transaction amount, original and new balances of the account. Each transaction is labeled as fraudulent or not (`isFraud`).

## Implementation
The script is implemented in Python, utilizing libraries such as `pandas` for data handling and `sklearn` for logistic regression modeling and evaluation. The process involves:

1. **Data Loading and Preprocessing**: The dataset is loaded using pandas, and necessary preprocessing steps are applied.

2. **Feature Selection**: Features including `amount`, `oldbalanceOrg`, and `newbalanceOrig` are selected for the model.

3. **Model Training and Testing**: The dataset is split into training and testing sets, and logistic regression is applied.

4. **Model Evaluation**: The model's performance is evaluated using metrics like precision, recall, F1-score, and confusion matrix.

## Results
The classification report details the model's performance:

- **Class 0 (Non-Fraudulent)**:
  - Precision: 100%
  - Recall: 100%
  - F1-Score: 100%

- **Class 1 (Fraudulent)**:
  - Precision: 71%
  - Recall: 98%
  - F1-Score: 83%

- **Overall Model Performance**:
  - Accuracy: 100%
  - Macro Average: 86% Precision, 99% Recall, 91% F1-Score
  - Weighted Average: 100% for all metrics

## Interpretation
- The model excels in identifying non-fraudulent transactions with perfect precision and recall.
- While effective in identifying fraudulent transactions, it shows some limitations in precision, indicating false positives.
- The high recall for fraudulent transactions is advantageous in critical applications like fraud detection.
- The overall accuracy might be skewed due to class imbalance in the dataset.

## Conclusion
This logistic regression model demonstrates substantial effectiveness in detecting fraudulent transactions in financial data. It performs exceptionally well in recognizing non-fraudulent transactions and very well in detecting fraudulent ones, albeit with some false positives. The model is particularly suitable for scenarios where the cost of missing a fraudulent transaction is high. However, users should be cautious about the high overall accuracy, which might be influenced by the class imbalance in the dataset.
