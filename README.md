# 🌍 CO₂ Emissions Prediction

## 📖 Project Overview

This project predicts **vehicle CO₂ emissions (g/km)** using a structured dataset of numerical and categorical features. The workflow includes **Exploratory Data Analysis (EDA), preprocessing, feature engineering, model training, hyperparameter tuning, PCA, and ensemble methods** to achieve high prediction accuracy.

---

## ⚙️ Technologies Used

* **Python 3**
* **Pandas, NumPy** – Data handling
* **Matplotlib, Seaborn** – Data visualization
* **Scikit-learn** – Preprocessing, modeling, evaluation
* **XGBoost** – Advanced regression model
* **Ensemble Methods** – Voting & Stacking

---

## 📊 Workflow

### 1. Data Preprocessing

* Checked missing values and data types
* Split features into **numeric** and **categorical**
* Outlier detection & handling with **IQR + Winsorization**
* Encoded categorical features with **Label Encoding**
* Normalized features using **RobustScaler**

### 2. Exploratory Data Analysis

* **Univariate Analysis**: Histograms, boxplots, skewness, kurtosis, normality test
* **Bivariate Analysis**: Spearman correlation with target variable
* **Multivariate Analysis**: Pairplots, correlation heatmap

### 3. Modeling

Implemented multiple regressors:

* **Decision Tree Regressor**
* **Linear Regression**
* **Random Forest Regressor**
* **XGBRegressor**

Metrics evaluated: **R² Score, Mean Absolute Error (MAE), Mean Squared Error (MSE)**

### 4. Ensemble Learning

* **Voting Regressor** (combined DT, LR, RF, XGB)
* **Stacking Regressor** (meta-model: Ridge Regression)

### 5. Hyperparameter Tuning

* **RandomizedSearchCV** for Decision Tree, Random Forest, and XGBoost
* Optimized parameters such as `max_depth`, `n_estimators`, `learning_rate`, `subsample`, etc.

### 6. Dimensionality Reduction with PCA

* Reduced features into **3 principal components**
* Re-trained models with PCA features and compared performance

### 7. Model Comparison

Evaluated performance **before & after tuning**, **with/without PCA**, and **ensemble methods**.

---

## 📈 Results

| Condition                     | R² Score | MAE  | MSE    |
| ----------------------------- | -------- | ---- | ------ |
| Without PCA (Before Tuning)   | 0.9942   | 2.09 | 19.79  |
| Without PCA (After Tuning)    | 0.9936   | 2.16 | 22.05  |
| Ensemble (Voting Regressor)   | 0.9882   | 3.57 | 40.58  |
| Ensemble (Stacking Regressor) | 0.9930   | 2.12 | 23.86  |
| With PCA (Before Tuning)      | 0.9517   | 8.72 | 165.37 |
| With PCA (After Tuning)       | 0.9587   | 7.99 | 141.48 |

✅ **Best Performance**: Decision Tree / Random Forest (without PCA, tuned) with R² ≈ **0.994**
⚠️ PCA reduced performance but improved dimensionality efficiency.
📊 Ensemble methods gave competitive results but did not surpass tuned Random Forest.

---

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:

   ```bash
   jupyter notebook
   ```

---

✍️ **Author**: Gervasius Russell
🎓 **Major**: Data Science, BINUS University
