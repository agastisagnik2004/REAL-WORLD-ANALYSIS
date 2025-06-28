# REAL-WORLD-ANALYSIS
# Linear Regression model applied as well as PCA analysis,Feature Selection, VIF also present
# Salary Prediction using Machine Learning

## 📌 Objective
To analyze employee salary components and predict Net Pay using machine learning, while identifying and resolving multicollinearity issues in the dataset.

📍 Data Source: Collected from a real-world institute — "NEW INTEGRATED GOVT. SCHOOL", RAMNAGAR-2.  
Note: The "Name of Employee" column has been anonymized for data privacy and protection.

---

## 📁 Dataset Overview

The dataset includes the following features:

- Name of Employee
- Basic Pay
- DA (@ 18%)
- HRA (@ 12% of Basic Pay)
- Medical Allowance
- Admissible Pay Per Month
- P.Tax
- Income Tax
- P.F
- Insurance
- Net Pay (Target Variable)

---

## 🧹 Data Preprocessing Steps

- Removed extra whitespaces from column names to prevent `KeyError`.
- Dropped multicollinear or derived columns:
  - DA (@ 18%)
  - HRA (@ 12% of Basic Pay)
  - Admissible Pay Per Month
  - Insurance
- Applied `StandardScaler` to:
  - Basic Pay
  - P.Tax
  - Medical Allowance

---

## 🤖 Modeling

- Algorithm: Linear Regression
- Features Used:
  - Basic Pay (Scaled)
  - P.Tax
  - Medical Allowance
- Target Variable: Net Pay (Scaled)

---

## 📈 Model Evaluation

- RMSE (Root Mean Squared Error): Low — indicating strong predictive power.
- R² Score: High — indicating a strong linear correlation between input features and target.

---

## 🔮 New Data Prediction Example

**Input:**
- Basic Pay = ₹40000
- P.Tax = ₹800
- Medical Allowance = ₹200

**Predicted Net Pay**: ₹23026.50

---

## 📊 Visualization

- Used `seaborn.lineplot()` to compare Actual vs Predicted Net Pay.
- Helped visualize the model's performance on test data.

---

## ⚠️ Issues Faced and Fixes

| Issue                                     | Solution                                 |
|------------------------------------------|------------------------------------------|
| `KeyError` due to space in column names  | Used `df.columns.str.strip()`            |
| Multicollinearity (VIF > 1000)           | Dropped derived/redundant features       |
| Feature mismatch in prediction           | Ensured new data matched training format |
| Warnings from `scikit-learn`             | Used `warnings.filterwarnings('ignore')` |

---

## ✅ Conclusion

- Linear Regression successfully predicted Net Pay using selected features.
- Model performed well after handling multicollinearity and applying scaling.
- Predictions are accurate and reliable when input data is properly formatted.

