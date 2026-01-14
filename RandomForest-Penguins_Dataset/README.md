# **Random Forest Classifier on the Palmer Penguins Dataset**

---

## **Project Overview**
This project demonstrates a robust machine learning workflow for a multiclass classification task using the Random Forest algorithm. The goal is to accurately predict the species of a penguin (Adelie, Chinstrap, or Gentoo) based on its morphological measurements and geographical location.
The entire analysis, from Exploratory Data Analysis (EDA) to model evaluation, is contained within the included Jupyter Notebook: `Random_Forest_Penguins_Dataset.ipynb`.

---

## **Model & Methodology**

**The Random Forest Classifier**
The Random Forest is an ensemble learning method that operates by constructing a multitude of decision trees at training time. This project utilizes its robust nature and ability to handle both numerical and categorical data effectively.

**Machine Learning Pipeline**
A core component of this project is the use of the `ColumnTransformer` and `Pipeline` objects from scikit-learn. This ensures:
1. Consistency: All preprocessing steps are applied uniformly to both training and test data.
2. No Data Leakage: Imputation and scaling parameters are calculated only on the training data, preventing data leakage from the test set.

**Preprocessing Steps:**
| Feature Type | Columns                                                               | Transformation                                                  |
| ------------ | --------------------------------------------------------------------- | --------------------------------------------------------------- |
| Numerical    | `bill_length_mm`, `bill_depth_mm`, `flipper_length_mm`, `body_mass_g` | Median imputation for missing values                            |
| Categorical  | `island`, `sex`                                                       | Mode imputation for missing values followed by One-Hot Encoding |

---

## **Key Results**
The Random Forest model achieved high and stable performance on the classification task.
| Metric         | Result (Example)                          |
| -------------- | ----------------------------------------- |
| Accuracy Score | 97.7% on the test set                     |
| Robustness     | Strong F1-scores across all three species |

---

## **Feature Importance**
Analysis of the Random Forest feature importances clearly indicated that certain morphological characteristics are the most crucial predictors of species:

1. **Flipper Length**
2. **Bill Depth**
3. **Bill Length**

This aligns with known biological differences between the Gentoo, Chinstrap, and Adelie species.