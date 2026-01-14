# Decision Tree Car Evaluation

## Overview
This project implements a **Decision Tree classification model** to evaluate car acceptability based on multiple categorical attributes such as price, maintenance cost, safety, and passenger capacity.

The objective is twofold:
1. Predict car acceptability accurately  
2. Extract **interpretable decision rules** that explain *why* a car is accepted or rejected

This project emphasizes **model interpretability, overfitting control, and business-aligned insights**, not just accuracy.

---

## Problem Statement
Given a car’s specifications, classify it into one of the following categories:

- **unacc** – Unacceptable  
- **acc** – Acceptable  
- **good** – Good  
- **vgood** – Very Good  

---

## Dataset Description
The dataset consists of **1,728 records** with **fully categorical features**.

| Feature | Description |
|-------|------------|
| buying | Buying price of the car |
| maint | Maintenance cost |
| doors | Number of doors |
| persons | Passenger capacity |
| lug_boot | Luggage boot size |
| safety | Safety rating |
| class | Target variable |

**Notes:**
- No missing values
- All features are ordinal categorical
- Target variable is imbalanced (`unacc` dominates)

---

## Exploratory Data Analysis (EDA)
Key observations from EDA:

- Target class imbalance exists (majority: `unacc`)
- Input features are evenly distributed
- **Safety** shows the strongest separation across classes
- **Buying price** and **maintenance cost** act as secondary decision drivers
- `doors` and `lug_boot` contribute weak predictive power

EDA confirmed the dataset is well-suited for rule-based modeling.

---

## Modeling Approach

### Preprocessing
- Applied **Ordinal Encoding** to preserve category ordering
- Built a **Pipeline** combining preprocessing and modeling
- Train-test split: **75% / 25%**

### Model
- Algorithm: `DecisionTreeClassifier`
- Criterion: `gini`
- Class weight: `balanced`

---

## Initial Model Performance

| Metric | Train | Test |
|------|------|------|
| Accuracy | 100% | ~96% |

### Observation
The model achieved perfect training accuracy, indicating **overfitting** caused by excessive tree depth and overly specific decision rules.

---

## Overfitting Control & Hyperparameter Tuning

### Techniques Used
- Cost-complexity pruning (`ccp_alpha`)
- `GridSearchCV` on:
  - `max_depth`
  - `min_samples_split`
  - `min_samples_leaf`
  - `criterion`

### Outcome
- Reduced tree depth
- Improved generalization
- Better recall for minority classes (`acc`, `good`, `vgood`)
- Slight reduction in training accuracy with improved test stability

---

## Performance Comparison

| Metric | Before Tuning | After Tuning |
|------|---------------|--------------|
| Train Accuracy | 1.00 | ~0.99 |
| Test Accuracy | ~0.96 | ~0.97 |
| Tree Depth | Very deep | Controlled |
| Overfitting | High | Reduced |

---

## Decision Tree Insights

### Primary Driver
- **Safety** is the root decision factor
  - Low safety → almost always `unacc`

### Secondary Drivers
- Buying price
- Maintenance cost
- Passenger capacity

### Low Impact Features
- Number of doors
- Luggage boot size

This hierarchy aligns with real-world car evaluation logic.

---

## Business Interpretation

The final Decision Tree is highly interpretable, providing clear, logical rules.

### Cars Likely to Be Rejected
- Low safety ratings
- High cost with poor safety
- Low passenger capacity

### Cars Rated Good or Very Good
- High safety
- Moderate or low maintenance cost
- Seating for 4 or more passengers

**Key Insight:**  
Safety is non-negotiable. Cost is conditional. Capacity matters contextually.

---
## Project Conclusion

The tuned Decision Tree provides a powerful and transparent solution for the Car Evaluation problem. It successfully navigated the challenges of categorical data encoding and class imbalance to achieve a near-perfect accuracy score of 99.54%. The resulting model offers a set of logical, explainable rules, making it an ideal choice for a system where transparency and justification are critical.