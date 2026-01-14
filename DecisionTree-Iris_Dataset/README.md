# Decision Tree Classifier on Iris Dataset

## Project Overview

This project implements a Decision Tree Classifier to accurately categorize the three species of Iris flowers—Iris Setosa, Iris Versicolor, and Iris Virginica—based on measurements of their sepals and petals.

The goal is to build a highly accurate yet fully transparent and interpretable model, demonstrating the power of Decision Trees for classification tasks with clean, balanced data.

**Iris Dataset – Feature Description**
| **Feature Name**  | **Description**            | **Data Type** |
| ----------------- | -------------------------- | ------------- |
| sepal length (cm) | Length of the sepal        | float64       |
| sepal width (cm)  | Width of the sepal         | float64       |
| petal length (cm) | Length of the petal        | float64       |
| petal width (cm)  | Width of the petal         | float64       |
| species (Target)  | Species of the Iris flower | object        |

### Key Dataset Characteristics

* **Total Observations: 150**
* **Missing Values: None**
* **Class Balance: Perfectly balanced, with 50 samples for each of the three species.**

## Methodology

### Data Preparation
1. **Data Loading:** The Iris dataset was loaded directly using `sklearn.datasets.load_iris().`
2. **Exploratory Data Analysis (EDA):** Boxplots were used to visualize feature distribution across species, confirming that:
   - Iris Setosa is highly separable from the other two species.
   - Iris Versicolor and Iris Virginica show some overlap, particularly in sepal measurements.
3. **Train-Test Split:** The data was split into training and testing sets to evaluate generalization capability.

### Modeling

- Model: DecisionTreeClassifier from scikit-learn.
- Training: The classifier was trained on the four continuous features (sepal length/width, petal length/width) to predict the species label.

## Results and Performance

The model achieved high accuracy, successfully distinguishing all Setosa samples and making only minor errors between the more similar Versicolor and Virginica classes.

**Overall Test Accuracy: 95.56%**

| Class (Species) | Precision | Recall | F1-Score | Support |
| :--- | :--- | :--- | :--- | :--- |
| **Iris Setosa** | 1.00 | 1.00 | 1.00 | 18 |
| **Iris Versicolor**| 0.82 | 1.00 | 0.90 | 9 |
| **Iris Virginica**| 1.00 | 0.89 | 0.94 | 18 |

### Decision Tree Visualization

This visualization is the core component of the project, clearly showing the splitting nodes based on features like Petal Length and Petal Width.

## Model Interpretability
One of the greatest benefits of the Decision Tree model is its interpretability. The model learned a simple set of rules, visualized below:

**Key Decision Rules Learned**

The model determined that Petal Length and Petal Width are the most important features for classification:

1. Rule for Setosa: If `Petal Length (cm) <= 2.45`, the species is Iris Setosa (Perfectly separated).

2. Rule for Virginica: If `Petal Length (cm) > 5.0` AND `Petal Width (cm) > 1.75`, the species is highly likely to be Iris Virginica.

This outcome is consistent with domain knowledge that petal characteristics are the most differentiating features for these species.

## Project Conclusion
The project successfully deployed a Decision Tree Classifier that achieved a high accuracy of **95.56%** on the Iris classification task. The final model is:

* Accurate: High performance metrics across all classes.
* Interpretable: Provides clear, logical, and biologically meaningful classification rules.
* Deployable: Simple and transparent, making it easy to explain and justify in a production environment.