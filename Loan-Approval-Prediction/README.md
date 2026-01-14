# **Loan Approval Prediction using Machine Learning**

## **Project Overview**
This project focuses on predicting loan approval outcomes using applicants’ financial, credit, and demographic information. Rather than optimizing for a single high-performing model, the objective is to build a **interpretable, and realistic machine learning pipeline** that mirrors how lending decisions are made in practice. Emphasis is placed on exploratory analysis, feature engineering, multicollinearity control, and cautious interpretation of model performance.

---

## **Dataset Description**
The dataset consists of **4,269 loan applications** with **13 features**, capturing applicant demographics, income, loan characteristics, credit score, and asset values.

**Target Variable**
- `loan_status`:  
  - `1` → Approved  
  - `0` → Rejected  

**Key Features**
- Demographics: `no_of_dependents`, `education`, `self_employed`
- Financial: `income_annum`, `loan_amount`, `loan_term`
- Credit: `cibil_score`
- Assets: residential, commercial, luxury, and bank asset values

The dataset exhibits **moderate class imbalance** (~62% approved, ~38% rejected) and no missing values.

---

## **Modeling Approach**
The modeling workflow followed a structured, professional pipeline:

1. **Data Cleaning & Encoding**
   - Removed identifier columns
   - Standardized categorical values and encoded them numerically

2. **Exploratory Data Analysis (EDA)**
   - Target vs feature analysis revealed strong overlap between approved and rejected cases
   - Financial magnitudes showed heavy right skew
   - Assets and loan amounts scaled strongly with income

3. **Multicollinearity Analysis**
   - Correlation matrix and VIF revealed severe redundancy among income, loan amount, and asset features
   - CIBIL score and demographic features remained independent

4. **Feature Engineering**
   - Consolidated asset variables into `total_assets`
   - Created ratio-based features:
     - `loan_to_income_ratio`
     - `assets_to_loan_ratio`
   - Dropped raw magnitude features to stabilize linear models
   - Revalidated multicollinearity using VIF (all features ≈ 1–2)

5. **Baseline Modeling**
   Three baseline models were evaluated using the same train–test split:
   - Logistic Regression (scaled)
   - Decision Tree (depth-capped)
   - Random Forest

---

## **Initial Model Performance**
- **Logistic Regression** achieved strong and realistic performance:
  - ROC-AUC ≈ **0.97**
  - Balanced precision and recall
- **Decision Tree and Random Forest** achieved near-perfect test performance.

---

## **Performance Comparison**
| Model | ROC-AUC | Interpretation |
|-----|--------|---------------|
| Logistic Regression | ~0.97 | Realistic, stable, interpretable |
| Decision Tree | ~1.00 | Recovers deterministic rules |
| Random Forest | ~1.00 | Strong but policy-driven |

Tree-based models clearly outperformed linear models numerically, but their results required deeper scrutiny.

---

## **Project Conclusion**
This project demonstrates an **end-to-end machine learning workflow** for a financial decision-making problem.
The analysis emphasizes:
- Interpretability
- Leakage awareness over metric inflation
- Sound feature engineering over raw magnitude dominance