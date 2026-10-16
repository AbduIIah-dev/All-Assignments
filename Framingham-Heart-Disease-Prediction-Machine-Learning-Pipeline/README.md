# 🫀 Framingham Heart Disease Prediction & Analysis

A comprehensive Machine Learning pipeline for predicting the 10-year risk of **Coronary Heart Disease (CHD)** using the Framingham Heart Study dataset. 

This repository demonstrates rigorous exploratory data analysis (EDA), data preprocessing, prevention of data leakage through Scikit-Learn pipelines, handling class imbalance using SMOTE, and model evaluation across multiple classifiers.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Dataset Information](#-dataset-information)
- [Key Features & Methodology](#-key-features--methodology)
  - [1. Data Preprocessing & Leakage Prevention](#1-data-preprocessing--leakage-prevention)
  - [2. Class Imbalance Mitigation](#2-class-imbalance-mitigation)
  - [3. Machine Learning Models](#3-machine-learning-models)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [How to Run](#-how-to-run)
- [Results & Model Performance](#-results--model-performance)
- [Key Insights](#-key-insights)
- [Technologies Used](#-technologies-used)
- [License](#-license)

---

## 🔬 Overview
Coronary Heart Disease (CHD) remains one of the leading causes of mortality globally. Early identification of high-risk patients enables targeted medical interventions. 

This project builds a predictive workflow to classify patients' 10-year risk of developing CHD based on demographic, behavioral, and medical features. The modeling pipeline strictly prevents **data leakage** by ensuring feature transformations (imputation, scaling) and oversampling (`SMOTE`) are fitted solely on the training data.

---

## 📊 Dataset Information
The dataset originates from the **Framingham Heart Study** and contains over **4,200 records** with 15 clinical and behavioral features:

| Feature Category | Features |
| :--- | :--- |
| **Demographics** | `male` (Sex), `age`, `education` |
| **Behavioral** | `currentSmoker`, `cigsPerDay` |
| **Medical History** | `BPMeds`, `prevalentStroke`, `prevalentHyp`, `diabetes` |
| **Physical Examination** | `totChol`, `sysBP`, `diaBP`, `BMI`, `heartRate`, `glucose` |
| **Target Label** | `TenYearCHD` (0 = No Risk, 1 = High Risk of CHD) |

> ⚠️ **Class Imbalance Note:** The target feature `TenYearCHD` is highly imbalanced (~85% non-CHD, ~15% CHD), requiring special handling like `SMOTE` and metric selection tailored to recall and PR-AUC.

---

## 🛠️ Key Features & Methodology

### 1. Data Preprocessing & Leakage Prevention
* **Train-Test Split First:** The dataset is split using stratified sampling before any missing value imputation or scaling.
* **Pipeline Integration:** `sklearn.pipeline.Pipeline` / `imblearn.pipeline.Pipeline` is used to chain `SimpleImputer` / `KNNImputer`, `StandardScaler`, and classification algorithms. This ensures that parameters computed on $X_{train}$ are never leaked to $X_{test}$.

### 2. Class Imbalance Mitigation
* Applied **SMOTE (Synthetic Minority Over-sampling Technique)** inside cross-validation folds and pipeline steps to prevent synthetic sample generation on validation sets.

### 3. Machine Learning Models
Evaluated multiple classification algorithms:
- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- XGBoost Classifier

---

## 📁 Project Structure

```bash
.
├── data/
│   └── framingham.csv           # Framingham Heart Disease Dataset
├── notebooks/
│   └── heart_disease_analysis.ipynb  # Primary Jupyter Notebook
├── src/
│   ├── data_preprocessing.py   # Pipeline building & imputation scripts
│   └── train.py                # Model training and evaluation
├── README.md                   # Project Documentation
├── requirements.txt            # Python Dependencies
└── .gitignore                  # Git Ignore File
