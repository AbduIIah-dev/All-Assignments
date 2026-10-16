# 🏡 House Price Prediction using Linear Regression

An end-to-end Machine Learning project focused on analyzing real estate data through Exploratory Data Analysis (EDA) and building a Supervised Learning model to predict housing prices.

## ✨ Project Steps & Implementation Details

* **Exploratory Data Analysis (EDA):** Performed detailed **Univariate Analysis** (analyzing single columns like target distribution) and **Bivariate Analysis** (analyzing relationships between independent features and `price`).
* **Data Cleaning & Preprocessing:** Maintained data integrity by handling missing/skewed structures, encoding categorical variables into numeric formats, and structuring features appropriately before training.
* **Feature Scaling:** Applied standard scaling techniques to ensure high-magnitude features (like `area`) don't bias the regression model against smaller integer inputs (like `bedrooms`, `bathrooms`).
* **Model Training & Evaluation:** Split the dataset into training and testing sets, trained a **Linear Regression** model, fed the preprocessed data, and evaluated the model by predicting on unseen test samples.

## 🛠️ Tech Stack & Libraries Used

* **Data Wrangling:** `pandas`, `numpy`
* **Data Visualization:** `seaborn`, `matplotlib` (Univariate histograms, Bivariate scatter plots, and trend analytics)
* **Machine Learning (Scikit-Learn):**
  * `train_test_split` (Data splitting)
  * `StandardScaler` / `MinMaxScaler` (Feature normalization)
  * `LinearRegression` (Core predictive model)
  * `metrics` ($R^2$ Score, MAE, MSE for evaluation)

## 📊 Standard Machine Learning Pipeline Followed

1. **Data Loading:** Importing and inspecting the raw housing dataset.
2. **EDA:** Visualizing correlations and feature distributions to understand patterns.
3. **Data Cleaning:** Encoding categorical text elements and normalizing ranges to prevent model distortions.
4. **Model Feeding & Prediction:** Training the Linear Regression line, feeding clean arrays, and generating final price predictions.

## 🚀 How to Run the Project

1. Clone this repository to your local system.
2. Open your Command Prompt (`CMD`) and navigate to this folder.
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Run the notebook file to view the EDA graphs, model training blocks, and prediction outputs.
