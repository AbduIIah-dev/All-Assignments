# Student Exam Score Prediction & Data Preprocessing

This repository contains a comprehensive data preprocessing and feature engineering workflow for a **Student Exam Score Prediction** dataset. The primary goal of this project is to clean, encode, and analyze raw student performance data, preparing it for Machine Learning regression models.

---

## 📌 Project Overview

Predicting student performance based on daily habits, parental background, and academic factors is a classic regression problem in Machine Learning. In this project, raw student dataset features—including categorical, ordinal, and binary attributes—are thoroughly inspected, cleaned, and converted into numerical formats using standard data science techniques.

---

## 🛠️ Key Data Preprocessing Steps

1. **Data Inspection & Cleaning:**
   * Loaded the dataset using `pandas`.
   * Evaluated dataset shape, column data types, and missing value counts.
   * Handled missing values in features like `parental_education_level`.

2. **Categorical Data Encoding:**
   * **One-Hot Encoding:** Applied to non-ordinal nominal categories like `gender`.
   * **Label Encoding:** Applied to binary categorical features (`part_time_job`, `extracurricular_participation`).
   * **Ordinal Encoding:** Applied to ordered categorical features (`diet_quality`, `parental_education_level`, `internet_quality`).

3. **Feature Correlation & Analysis:**
   * Calculated Pearson correlation coefficients between all preprocessed input features and the target variable (`exam_score`).
   * Evaluated feature importance and linear relationships to guide feature selection for modeling.



## 💻 Tech Stack & Tools

* **Language:** Python
* **Libraries:** `pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `warning`
* **Environment:** Jupyter Notebook
