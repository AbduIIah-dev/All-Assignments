# Fraud Detection Using Machine Learning

## 📌 Project Overview

This project focuses on building a machine learning system for detecting fraudulent transactions.

The dataset contains a highly imbalanced target variable, where fraudulent transactions are much fewer than non-fraudulent transactions. Therefore, different preprocessing and class-imbalance handling techniques were applied before training multiple machine learning classification models.

The main objective of this project is to compare multiple classification algorithms and select the best-performing model for fraud detection based on Accuracy, Precision, and Recall.

---

## 🎯 Objectives

- Perform data preprocessing and cleaning
- Handle categorical features using One-Hot Encoding
- Handle class imbalance using SMOTE
- Apply feature scaling using MinMaxScaler and StandardScaler
- Train multiple machine learning classification models
- Evaluate models using Accuracy, Precision, and Recall
- Compare model performance
- Select the best model for fraud detection

---

## 📊 Dataset

The target variable is:

`is_fraudulent`

The original target distribution is:

- Normal Transactions: 4,871
- Fraudulent Transactions: 129

This shows that the dataset is highly imbalanced, with fraudulent transactions representing only a small portion of the data.

---

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

### 1. Train-Test Split

The dataset was divided into training and testing sets using an 80/20 split.

Stratified splitting was used to maintain the class distribution in both sets.

### 2. Categorical Encoding

Categorical features were converted into numerical features using:

`OneHotEncoder`

The categorical columns included:

- gender
- country
- preferred_category

### 3. Handling Class Imbalance

SMOTE (Synthetic Minority Over-sampling Technique) was applied only to the training data.

The test data was kept unchanged to provide an unbiased evaluation of the models.

### 4. Feature Scaling

Two scaling techniques were tested:

- MinMaxScaler
- StandardScaler

---

## 🤖 Machine Learning Models

The following classification algorithms were compared:

- Logistic Regression
- Support Vector Classifier (SVC)
- Decision Tree Classifier
- Random Forest Classifier
- Bagging Classifier
- AdaBoost Classifier
- Gradient Boosting Classifier

---

## 📈 Evaluation Metrics

The models were evaluated using:

### Accuracy

Measures the overall percentage of correctly classified observations.

### Precision

Measures how many transactions predicted as fraudulent were actually fraudulent.

### Recall

Measures how many actual fraudulent transactions were successfully detected.

For this fraud detection problem, Recall was given higher importance because failing to detect a fraudulent transaction can be more important than incorrectly flagging a normal transaction.

---

## 🔍 Model Comparison

Each model was trained using both:

- MinMaxScaler
- StandardScaler

The results were stored in a DataFrame containing:

- Accuracy_Train
- Accuracy_Test
- Precision_Train
- Precision_Test
- Recall_Train
- Recall_Test

The models were then compared based on their test-set performance.

---

## 🏆 Best Model Selection

The final model was selected by giving higher priority to Test Recall, followed by Test Precision and Test Accuracy.

This approach was chosen because fraud detection is an imbalanced classification problem where detecting fraudulent transactions is more important than relying only on overall accuracy.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib
- Jupyter Notebook

---

## 📚 Key Learning Outcomes

Through this project, I learned how to:

- Preprocess real-world datasets
- Encode categorical variables
- Handle highly imbalanced classification data
- Apply SMOTE correctly
- Scale numerical features
- Train multiple classification algorithms
- Compare machine learning models
- Evaluate models using multiple performance metrics
- Select a suitable model based on the problem requirements

---

## 👩‍💻 Author

**Abdullah Sohail Nasir**

Machine Learning & Data Science Student
