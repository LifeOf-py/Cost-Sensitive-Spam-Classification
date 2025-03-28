# 🛡️ Cost-Sensitive Spam Classification

This project develops and evaluates binary classification models to detect spam emails, incorporating **cost-sensitive evaluation** to reduce false positives, which are much costlier in this scenario.

---

## 📌 Project Overview

- **Task**: Classify emails as spam (1) or not spam (0).
- **Goal**: Minimize costly false positives (non-spam marked as spam).
- **Dataset**: UCI Spambase (numeric email features).
- **Primary Metric**: **Custom Cost Function**  
  `Cost = 10 × False Positives + 1 × False Negatives`

---

## 🧰 Tools & Libraries
- Python, Jupyter Notebook
- `scikit-learn`
- `imbalanced-learn` (for SMOTE)
- `XGBoost`, `LightGBM`
- `matplotlib`, `seaborn` for plots

---

## 🧠 Modeling Strategy

- Used **Nested Cross-Validation** for robust model selection and tuning.
- Evaluated classifiers: Logistic Regression, KNN, Decision Tree, SVC, Random Forest, Gradient Boosting, XGBoost, LightGBM, Neural Net.
- Custom scoring function penalized false positives 10x more.

---

## ✅ Results

- Best model: **LightGBM**
- AUC ≈ 0.987  
- Avg Cost ≈ 0.279  
- Excellent precision-recall balance with minimal false positives
- Diagnostic plots: Confusion Matrix, PR Curve, ROC Curve, Lift Curve

---

## 💼 Business Value

- Cost-sensitive classification mirrors real-world needs in spam detection
- Reduces risk of missing important (non-spam) emails
- Demonstrates ability to implement domain-specific evaluation

---

> 📂 Explore the full notebook: `cost_based_classification.ipynb`
