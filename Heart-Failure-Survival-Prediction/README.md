# Heart Failure Survival Prediction 🫀

This repository contains a Machine Learning workflow designed to predict heart failure mortality using patient clinical records. The project handles severe class imbalance using SMOTE and optimizes feature scaling for improved model evaluation.

---

## 📌 Features Included
- **Outlier Handling**: IQR (Interquartile Range) method used to cap numerical outliers.
- **Feature Selection**: High-impact clinical features selected (`time`, `serum_creatinine`, `ejection_fraction`, `age`, `serum_sodium`).
- **Class Balancing**: Applied **SMOTE** (Synthetic Minority Over-sampling Technique) on training data to address target variable imbalance.
- **Feature Scaling**: Scaled inputs using `MinMaxScaler` for optimal convergence.
- **Model Training**: Evaluated performance using classification algorithms like Logistic Regression.

---

## 📁 Dataset Details
The dataset used is the **Heart Failure Clinical Records Dataset**, containing key clinical parameters such as:
- **`time`**: Follow-up period (days)
- **`serum_creatinine`**: Level of serum creatinine in the blood (mg/dL)
- **`ejection_fraction`**: Percentage of blood leaving the heart at each contraction
- **`age`**: Patient age
- **`serum_sodium`**: Level of serum sodium in the blood (mEq/L)
- **`DEATH_EVENT`**: Target variable (0 = Survived, 1 = Deceased)

---

## 🛠️ Project Structure & Workflow
1. **Data Preprocessing**: Handling missing values and numerical outliers.
2. **Exploratory Data Analysis (EDA)**: Understanding distributions and correlations.
3. **Resampling**: Balancing class distributions via SMOTE.
4. **Model Evaluation**: Metrics evaluated include Accuracy, Precision, Recall, F1-Score, and Confusion Matrix.

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/heart-failure-prediction.git](https://github.com/your-username/heart-failure-prediction.git)
