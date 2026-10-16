# Housing Price Prediction & Regression Analysis

A Machine Learning project focused on analyzing the Housing dataset, engineering informative features, handling spatial and categorical data, and evaluating multiple baseline regression models to predict median house values.

---

## 📌 Project Overview
The goal of this project is to build an end-to-end Machine Learning regression pipeline. It covers everything from preliminary Exploratory Data Analysis (EDA) and data preprocessing to feature engineering, scaling, and comparative evaluation of basic linear models, regularized regression, and decision trees.

---

## 🛠️ Data Preprocessing & Feature Engineering
- **Missing Value Imputation:** Fixed missing values in `total_bedrooms` using median imputation.
- **Categorical Encoding:** Applied One-Hot Encoding (`pd.get_dummies`) to handle the `ocean_proximity` feature.
- **Ratio Feature Engineering:** Created domain-specific engineered features to capture housing dynamics:
  - `rooms_per_household = total_rooms / households`
  - `bedrooms_per_room = total_bedrooms / total_rooms`
  - `population_per_household = population / households`
- **Feature Scaling:** Standardized numerical features using `StandardScaler` to prevent model bias and scale mismatch issues.

---

## 📊 Model Evaluation & Baseline Results

Multiple algorithms were implemented and tested to observe performance trade-offs, regularization effects, and overfitting tendencies:

| Model | Train $R^2$ Score | Test $R^2$ Score | Key Findings |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | ~0.679 | ~0.618 | Baseline benchmark; struggled with non-linear relationships |
| **Polynomial Regression** | ~0.803 | -67.73 | Experienced severe multicollinearity & overfitting without regularization |
| **Lasso / Ridge Regression** | ~0.678 | ~0.618 | Stable baseline performance, effectively constrained coefficient weights |
| **Polynomial + Lasso/Ridge** | ~0.775 | -0.602 | Partial regularization control on higher-degree polynomial features |
| **Decision Tree Regressor** | 1.000 | ~0.635 | Pure memorization/overfitting without hyperparameter depth constraints |

---

## 💡 Key Takeaways & Conclusion
1. **Feature Engineering Impact:** Adding ratio-based features enhanced dataset representation over raw spatial counts.
2. **Linear vs Non-Linear:** Linear models capped out around ~$0.64$ test $R^2$, demonstrating that house pricing contains complex non-linear feature interactions.
3. **Regularization Necessity:** Higher-degree Polynomial features require strict regularizers (Lasso/Ridge) to manage multicollinearity and prevent negative $R^2$ evaluation scores.

---

## 💻 Tech Stack
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn
