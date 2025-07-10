# Telecom-Customer-Churn-Prediction

# 📊 Customer Survival Analysis for Telecom Churn

This project implements a real-world **customer survival prediction system** using **Kaplan-Meier Estimator**, **Cox Proportional Hazards Model**, and **Random Forest Classifier** on a telecom dataset to estimate **how long a customer will stay before churning**.

---

## Problem Statement

Telecom companies lose millions annually due to customer churn. Traditional classification models only predict **if** a customer will churn — but businesses need to know:

> **"When is a customer likely to churn?"**

This project answers that using **Survival Analysis** to predict **time-to-churn** and drive proactive retention strategies.

---

###  Key Features
| Feature             | Description                                     |
|---------------------|-------------------------------------------------|
| `tenure`            | Customer lifetime in months (used as `duration`) |
| `Churn`             | Whether the customer churned (`Yes`/`No`)       |
| `MonthlyCharges`    | Monthly billing amount                          |
| `TotalCharges`      | Total amount charged                            |
| `Contract`          | Month-to-month / One year / Two year           |
| `PaymentMethod`     | Credit card / Electronic check / etc.          |
| `OnlineSecurity`    | Whether online security is enabled              |
| `TechSupport`       | Whether tech support is enabled                 |

---

##  Techniques Used

### 1. **Kaplan-Meier Estimator**
- Visualizes survival probability over time.
- Non-parametric, good for cohort comparisons.

### 2. **Cox Proportional Hazards Model**
- Semi-parametric regression model.
- Estimates **hazard ratios** for features affecting churn risk.
- Helps understand **which features increase/decrease risk over time**.

### 3. **Random Forest Classifier**
- Determines **feature importance** for churn prediction.
- Used for **classification-based evaluation** and performance comparison.

---

## 📊 Evaluation Metrics

| Metric            | Purpose                                              |
|-------------------|------------------------------------------------------|
| **Concordance Index (C-index)** | Measures how well the Cox model ranks risks |
| **ROC AUC Score** | Evaluates classification performance of Random Forest |
| **P-values**      | Tests statistical significance of each feature       |
| **Hazard Ratios** | Interprets relative risk contributed by features     |

---

##  Workflow Summary

```mermaid
flowchart TD
    A[Load Dataset] --> B[Preprocessing & Cleaning]
    B --> C[Feature Engineering]
    C --> D[Kaplan-Meier Survival Curve]
    C --> E[Cox Proportional Hazards Model]
    C --> F[Random Forest Feature Importance]
    E --> G[Survival Curve Plotting]
    F --> H[ROC AUC Evaluation]
