# Customer-Churn-Prediction
# Telecom Customer Churn Prediction & Feature Power Analysis

## 🎯 Business Objective
Our telecom business is experiencing a severe customer retention crisis, with a baseline churn rate of **49.2%**. The primary objective of this project was to engineer an end-to-end machine learning pipeline to identify at-risk customers early, allowing the marketing team to deploy proactive retention campaigns.

---

## 🛠️ Data Pipeline & Engineering
**Data Diagnostics:** Analyzed a dataset of 5,880 unique customer records across demographic, billing, and services categories. Verified numerical continuous variables (`Tenure`, `MonthlyCharges`, `TotalCharges`) for mathematical consistency.
**Exploratory Data Analysis (EDA):** Discovered an atypical business pattern where customer attrition remained uniform (~50%) regardless of contract obligations (Month-to-month vs. 1-Year vs. 2-Year contracts).
**Feature Processing:** Utilized One-Hot Encoding (`pd.get_dummies`) to translate categorical text fields into a 30-feature numerical matrix optimized for machine learning algorithms.

---

## 🤖 Model Performance & Evaluation

The processed dataset was split into an 80/20 train-test ratio. Two distinct algorithmic paradigms were trained and rigorously evaluated focusing on **Churn Recall (Class 1)**:

### 1. Baseline Model: Random Forest Classifier
**Accuracy:** 50%
**Churn Recall:** 44%
**Analysis:** The model struggled to differentiate stayers from churners, operating at a level equivalent to random chance.

### 2. Advanced Model: XGBoost Classifier (Gradient Boosting)
**Accuracy:** 50%
  **Churn Recall:** 45%
  **Analysis:** Transitioning to sequential gradient boosting yielded no significant performance delta. 

---

## 💡 Key Analytical Findings & Strategic Recommendations

### The Verdict: Data Limitations, Not Code
When an advanced, non-linear classifier like XGBoost fails to outperform a coin-flip baseline on a perfectly balanced dataset, it points to an architectural data challenge: **the current features lack predictive power.** The demographic and standard billing attributes currently captured do not contain the behavioral variance required to predict customer departure.

### Next Steps & Strategic Roadmap
To transform this into a highly accurate predictive tool, the next iteration of the project requires the acquisition of richer behavioral data columns from our engineering and support systems:
1. **Network Quality Metrics:** Integrating dropped call rates, average data speeds, and network latency metrics.
2. **Customer Friction Signals:** Tracking the number of customer support calls and open technical friction tickets.
3. **Usage Velocity:** Engineering delta features that monitor sharp month-over-month drops in data consumption or talk time.

---
*Project successfully built, tested, and documented by a Forward-Thinking Data Scientist.*
