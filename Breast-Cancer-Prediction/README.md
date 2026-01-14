# **Breast Cancer Classification using Machine Learning**

## **Project Overview**

This project explored the Breast Cancer dataset with the objective of building a reliable binary classification model to distinguish between malignant and benign tumors using numerical features derived from cell nucleus characteristics.

## **Dataset Description**

- Source: Breast Cancer Wisconsin (Diagnostic) Dataset
- Samples: 569
- Target Variable:
  - M → Malignant
  - B → Benign
- Features: 30 continuous numerical features derived from cell nucleus characteristics:
  - Mean measurements (*_mean)
  - Standard error measurements (*_se)
  - Worst-case measurements (*_worst)
- Data Quality:
  - No missing values in predictive features
  - No duplicate records
  - One non-informative identifier column removed (id)
 
## **Modeling Approach**

The problem is formulated as a binary classification task.
The modeling strategy follows a structured pipeline:
1. Exploratory Data Analysis (EDA) to understand feature behavior and class separability
2. Feature scaling (where required)
3. Stratified train–test split to preserve class proportions
4. Evaluation of multiple baseline models using consistent preprocessing and metrics
Outlier removal was deliberately avoided, as extreme values reflect real biological variation.

## **Initial Model Performance**

Four baseline models were evaluated without hyperparameter tuning:

| Model               | ROC–AUC | Accuracy | Malignant Recall |
| ------------------- | ------: | -------: | ---------------: |
| Logistic Regression |  ~0.995 |    ~0.97 |             0.95 |
| SVM (RBF)           |  ~0.995 |    ~0.98 |             0.98 |
| Random Forest       |  ~0.995 |    ~0.98 |             0.98 |
| KNN                 |   ~0.98 |    ~0.96 |             0.90 |

All top-performing models achieved near-saturated ROC–AUC, indicating strong inherent class separability in the dataset.

## **Performance Comparison**

- Logistic Regression provides strong performance with high interpretability, making it suitable for transparent decision-making.
- SVM (RBF) and Random Forest marginally outperform Logistic Regression, offering better malignant recall and flexibility.
- KNN shows comparatively weaker recall for malignant cases and is not considered a final candidate.
Performance differences between the top models are small and not clinically significant, reinforcing that model choice should be driven by deployment needs rather than raw metrics alone.

## **Project Conclusion**

This project demonstrates that, on a clean and information-rich medical dataset, careful EDA, principled baseline modeling, and restrained optimization are sufficient to achieve excellent performance.