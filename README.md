# HSBC Hackathon 2024 - Fraud Detection System

This project was developed as part of the **HSBC Hackathon 2024**. The aim was to build an AI-powered fraud detection model capable of identifying fraudulent transactions in real-time. The system leverages historical transaction data to train the model, allowing it to detect anomalies and flag suspicious activities efficiently.

## 🚀 Project Overview

The core of this project is based on training two machine learning models—**XGBoost Classifier** and **Random Forest Classifier**—to predict whether a transaction is fraudulent (1) or non-fraudulent (0). These models were chosen for their robustness and effectiveness in handling large datasets with complex decision boundaries.

## ⚙️ Model Details & Configurations

### 1. **XGBoost Classifier**
- **Objective:** `binary:logistic`
  - This specifies the model is for a binary classification task where the output is either 0 (non-fraudulent) or 1 (fraudulent).
- **Evaluation Metric:** `logloss`
  - Logarithmic loss is used to measure the performance of the model. It evaluates how well the predicted probabilities align with the actual labels, providing insight into the model's probability calibration.
- **Use Label Encoder:** `False`
  - This avoids warnings related to deprecated label encoding functions in XGBoost, ensuring compatibility with newer versions.
- **Random State:** `42`
  - Setting the random state ensures that results are reproducible across multiple runs.

### 2. **Random Forest Classifier**
- **Criterion:** `gini`
  - The Gini index is used to measure the quality of a split in the decision trees. It helps build a robust classifier by reducing impurities in each decision.
- **Number of Estimators:** `100`
  - The model uses 100 decision trees to form an ensemble and improve prediction accuracy.
- **Max Depth:** `None`
  - Trees are expanded until all leaves are pure, allowing the model to capture complex patterns in the data.
- **Random State:** `42`
  - Ensures consistent results for model reproducibility.

## 🛠️ Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Khushitiwari08/HSBC-Hackathon-FraudDetection.git
   cd HSBC-Hackathon-FraudDetection
