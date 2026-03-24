# Project-Prediction-of-Annual-Solar-Energy-Production
# 🌞 Solar Energy Production Prediction

## 📌 Project Overview
This project focuses on predicting **annual solar energy production (kWh)** for solar installations using machine learning. The goal is to support data-driven decision-making in solar project planning, location selection, and investment optimization.

---

## 🎯 Objective
- Predict annual solar energy production
- Identify key factors influencing output
- Support better planning and ROI decisions

---

## 📊 Dataset Overview
- ~218,000 records
- 17 features including:
  - PV System Size (kWac/kWdc)
  - County, City, Zip, Utility
  - Developer, Metering Method
  - Installation Date

**Target Variable:**
- Estimated Annual PV Energy Production (kWh)

---

## 🧹 Data Preprocessing
- Handled missing values (drop + imputation)
- Removed irrelevant columns (Project ID, etc.)
- Extracted `year` and `month`
- Encoded categorical variables
- Applied log transformation to target

---

## ⚙️ Feature Engineering
- `year`, `month` → temporal features
- `log_energy` → normalized target
- `log_size` → scaled PV size
- `county_freq` → regional density

---

## 🤖 Models Used
- Random Forest Regressor (Final Model)
- XGBoost Regressor

---

## 📈 Model Evaluation

| Metric | Random Forest | XGBoost |
|--------|--------------|--------|
| MAE    | 1341         | 5718   |
| RMSE   | 70537        | 126922 |
| R²     | 0.956        | 0.857  |

---

## 🔁 Cross Validation
- 5-Fold Cross Validation
- Mean R² Score: **0.9989**

---

## 🔍 Feature Dependency Analysis

Model performance without PV System Size:
<b>R²: 0.956 → 0.716</b>


**Insight:**
- PV System Size is the dominant feature
- Other features still contribute meaningfully

---

## 📊 Key Insights
- System size is the primary driver of energy production
- Location influences efficiency
- Developer and metering method impact performance
- Model remains predictive even without dominant feature

---

## 📌 Feature Importance
- PV System Size (kWac) → highest impact
- log_size → strong contribution
- Metering Method → moderate impact
- Location features → secondary contribution

---

## 📈 Model Performance
- Strong alignment between actual and predicted values
- Works well across different system sizes
- Minor deviation at extreme values

---

## 💼 Business Impact
- Enables accurate energy forecasting
- Improves ROI estimation
- Supports better decision-making for:
  - System sizing
  - Location selection
  - Developer choice

---

## 🏁 Conclusion
- Achieved high accuracy (R² ≈ 0.96)
- Validated using cross-validation
- Demonstrates strong predictive capability

**Final Insight:**
This project not only predicts solar energy production but also provides meaningful insights into the key factors influencing it.

---

## 🚀 Future Improvements
- SHAP interpretability
- Advanced feature engineering
- Model deployment

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib, Seaborn

---
# Thank You
