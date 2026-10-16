# 💳 Credit Card Fraud Detection using Deep Learning (ANN) & Optuna

An end-to-end Deep Learning project that builds and optimizes an **Artificial Neural Network (ANN)** to detect fraudulent credit card transactions. The model addresses extreme class imbalance using **SMOTE** and leverages **Optuna** for automated hyperparameter tuning to maximize the **F1-Score**.

---

## 📌 Project Overview

Credit card fraud is a major challenge for financial institutions. Fraudulent transactions constitute a very small percentage of total transactions, making this a classic **highly imbalanced classification problem**. 

This project aims to:
1. **Preprocess and scale** transaction features effectively.
2. Address class imbalance using **Synthetic Minority Over-sampling Technique (SMOTE)**.
3. Construct a flexible **Artificial Neural Network (ANN)** with **TensorFlow / Keras**.
4. Perform automated hyperparameter optimization using **Optuna** to maximize the **F1-Score** on validation data.

---

## 📊 Dataset Description

The dataset used in this project is the widely benchmarked **Credit Card Fraud Detection Dataset** (available on Kaggle).

* **Total Transactions:** 284,807
* **Number of Features:** 31 (PCA-transformed features `V1` to `V28`, plus `Time`, `Amount`, and `Class`)
* **Target Variable (`Class`):**
  * `0`: Genuine Transaction (Non-Fraud)
  * `1`: Fraudulent Transaction (Fraud)
* **Class Imbalance:** Extreme imbalance (~0.17% fraud cases).

---

## ⚙️ Key Requirements & Dependencies

To run this notebook successfully, ensure you have the following Python libraries installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn imbalanced-learn tensorflow optuna
