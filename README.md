# Machine-Learning-Projects
This repository provides an overview of my key Machine Learning projects. Each project demonstrates different aspects of data analysis, machine learning, and visualization.

---

## Projects

1. **Decision Tree Classifier on Iris Dataset**
    - **Description:** Built an interpretable Decision Tree classification model to predict Iris flower species (Setosa, Versicolor, Virginica) using sepal and petal measurements. The project emphasizes model transparency and rule-based decision making on a clean, balanced dataset.
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Decision Tree Classifier
    - **Results:** Achieved 95.56% test accuracy, with perfect classification of Iris Setosa and minor confusion between Versicolor and Virginica. The model learned clear, biologically meaningful rules, identifying petal length and petal width as the most important features.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Desition_Tree_Iris_Datadet)

2. **Decision Tree Classifier on Car Evaluation**
    - **Description:** Developed a Decision Tree classification model to evaluate car acceptability (unacc, acc, good, vgood) based on categorical attributes such as safety, price, maintenance cost, and passenger capacity.
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Graphviz, Decision Tree Classifier
    - **Results:** After applying ordinal encoding, class weighting, and cost-complexity pruning, the tuned Decision Tree achieved ~99.5% test accuracy with improved generalization and reduced overfitting.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Decision_Tree_Car_Evaluation)
  
3. **Random Forest Classifier on the Palmer Penguins Dataset**
    - **Description:** Built a robust multiclass classification model using Random Forest to predict penguin species (Adelie, Chinstrap, Gentoo) based on morphological measurements and location. The project emphasizes a leakage-safe machine learning pipeline with proper preprocessing, imputation, and encoding.
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Random Forest Classifier, ColumnTransformer, Pipeline
    - **Results:** Achieved 97.7% test accuracy with strong and balanced F1-scores across all three species.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Ramdom_Forest_Penguins_Dataset)
  
4. **Concrete Compressive Strength Prediction (Random Forest Regression)**
    - **Description:** Built a regression model to predict concrete compressive strength (MPa) using mix composition and curing age. The project emphasizes EDA-driven model selection, bias–variance trade-offs, and generalization-focused validation rather than aggressive hyperparameter tuning on a small, real-world engineering dataset.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Linear Regression, Random Forest Regressor (OOB Validation)
    - **Results:** A baseline Linear Regression achieved a test R² of 0.63, while the final Random Forest model improved performance to 0.87 test R² with ~40% error reduction (RMSE: 9.8 → 5.83 MPa, MAE: 7.75 → 4.25 MPa). The Random Forest also achieved a strong OOB R² of ~0.90, indicating stable generalization. Feature importance analysis identified age and cement as dominant predictors, consistent with domain knowledge.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Concrete_Compressive_Strength_Prediction)
  
5. **Telco Customer Churn Prediction (Random Forest Classification)**
   - **Description:** Developed a customer churn prediction system using a Random Forest classifier to identify customers at risk of churn in a subscription-based telecom business. The project emphasizes business-aligned modeling, combining target encoding, out-of-bag (OOB) validation, and decision threshold optimization to prioritize early churn detection over raw accuracy.
   - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Random Forest Classifier, Target Encoding, OOB Validation
   - Results: The final Random Forest model achieved an OOB score of ~0.76, ROC-AUC of ~0.84, and accuracy of ~0.78, demonstrating strong ranking performance and generalization. By optimizing the decision threshold to 0.35, churn recall improved to ~67%, aligning predictions with business priorities where missing a churner is more costly than a false alert. Feature importance analysis identified tenure, contract type, internet service, and online security as the strongest churn drivers.
   - **Project Link:** [View Repository](https://github.com/PranayDomal/Telco_Customer_Churn_Prediction)
  
6. **Linear Regression on Advertising Dataset**
    - **Description:** Applied Simple and Multiple Linear Regression to analyze how TV, Radio, and Newspaper advertising spend influence product sales, focusing on a correct, assumption-driven regression workflow and model interpretability.
    - **Results:** TV advertising alone explained ~67% of sales variance (R² ≈ 0.68), while the Multiple Linear Regression model improved performance to R² ≈ 0.91, significantly reducing prediction error. TV and Radio emerged as strong predictors, whereas Newspaper showed minimal impact.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Linear Regression, Statsmodels
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Advertising_Sales_Prediction)
  
7. **Mall Customers Segmentation using K-Means Clustering**
    - **Description:** Applied K-Means clustering to segment mall customers based on annual income and spending behavior, to identify clear, behavior-driven customer groups using Elbow Method and Silhouette Analysis.
    - **Results:** Identified 5 well-separated customer segments with a peak Silhouette Score of ~0.55, capturing distinct spending patterns such as high-value customers, careful high-income customers, and impulsive low-income spenders. The clusters are interpretable and suitable for targeted marketing strategies.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, K-Means Clustering, StandardScaler
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Mall_Customers-KMeans)
