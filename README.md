# Machine-Learning-Projects
This repository provides an overview of my key Machine Learning projects. Each project demonstrates different aspects of data analysis, machine learning, and visualization.

---

## Projects

1. **Salary Prediction using Machine Learning**
    - **Description:** Built an end-to-end machine learning pipeline to predict employee salaries using professional and demographic attributes
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Linear Regression, Random Forest Regressor, ColumnTransformer, Pipeline
    - **Results:** Linear Regression achieved R² ≈ 0.58 with higher error, serving as an interpretable baseline, while the Random Forest model improved performance to R² ≈ 0.91, reducing MAE from ~$22.9K to ~$8.6K.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Salary-Prediction)

2. **Loan Approval Prediction using Machine Learning**
    - **Description:** The aim of this project is to build and evaluate a machine learning model that predicts the likelihood of loan approval
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, Logistic Regression, Decision Tree, Random Forest
    - **Results:** Logistic Regression achieved a realistic ROC–AUC of ~0.97 with balanced precision and recall, while tree-based models reached near-perfect scores by recovering deterministic policy rules embedded in the data.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Loan-Approval-Prediction)

3. **Breast Cancer Classification using Machine Learning**
    - **Description:** Developed and evaluated multiple baseline machine learning models to classify breast tumors as malignant or benign.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Logistic Regression, SVM (RBF), Random Forest, KNN
    - **Results:** Baseline models achieved near-perfect ROC–AUC (~0.995) and ~97–98% accuracy without hyperparameter tuning.
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Breast-Cancer-Prediction)
  
7. **Concrete Compressive Strength Prediction (Random Forest Regression)**
    - **Description:** Built a regression model to predict concrete compressive strength (MPa) using mix composition and curing age.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Linear Regression, Random Forest Regressor (OOB Validation)
    - **Results:** A baseline Linear Regression achieved a test R² of 0.63, while the final Random Forest model improved performance to 0.87 test R² with ~40% error reduction (RMSE: 9.8 → 5.83 MPa, MAE: 7.75 → 4.25 MPa).
    - **Project Link:** [View Repository](https://github.com/PranayDomal/Concrete_Compressive_Strength_Prediction)
  
8. **Telco Customer Churn Prediction (Random Forest Classification)**
   - **Description:** Developed a customer churn prediction system using a Random Forest classifier to identify customers at risk of churn in a subscription-based telecom business.
   - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Random Forest Classifier, Target Encoding, OOB Validation
   - **Results:** The final Random Forest model achieved an OOB score of ~0.76, ROC-AUC of ~0.84, and accuracy of ~0.78, demonstrating strong ranking performance and generalization.
   - **Project Link:** [View Repository](https://github.com/PranayDomal/Telco_Customer_Churn_Prediction)
  
10. [**Mall Customers Segmentation using K-Means Clustering**](https://github.com/PranayDomal/Machine-Learning-Projects/tree/main/K-Means-Mall_Customers)
    - **Description:** Applied K-Means clustering to segment mall customers based on annual income and spending behavior, to identify clear, behavior-driven customer groups using Elbow Method and Silhouette Analysis.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, K-Means Clustering, StandardScaler
    - **Results:** Identified 5 well-separated customer segments with a peak Silhouette Score of ~0.55, capturing distinct spending patterns such as high-value customers, careful high-income customers, and impulsive low-income spenders. The clusters are interpretable and suitable for targeted marketing strategies.

9. [**Linear Regression on Advertising Dataset**](https://github.com/PranayDomal/Machine-Learning-Projects/tree/main/LinearRegression-Advertising_Dataset)
    - **Description:** Applied Simple and Multiple Linear Regression to analyze how TV, Radio, and Newspaper advertising spending influences product sales, focusing on a correct, assumption-driven regression workflow and model interpretability.
    - **Technologies Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Linear Regression, Statsmodels
    - **Results:** TV advertising alone explained ~67% of sales variance (R² ≈ 0.68), while the Multiple Linear Regression model improved performance to R² ≈ 0.91, significantly reducing prediction error. TV and Radio emerged as strong predictors, whereas Newspaper showed minimal impact.

6. [**Random Forest Classifier on the Palmer Penguins Dataset**](https://github.com/PranayDomal/Machine-Learning-Projects/tree/main/RandomForest-Penguins_Dataset)
    - **Description:** Built a robust multiclass classification model using Random Forest to predict penguin species (Adelie, Chinstrap, Gentoo) based on morphological measurements and location.
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Random Forest Classifier, ColumnTransformer, Pipeline
    - **Results:** Achieved 97.7% test accuracy with strong and balanced F1-scores across all three species.

5. [**Decision Tree Classifier on Car Evaluation**](https://github.com/PranayDomal/Machine-Learning-Projects/tree/main/DecisionTree-Car_Evalution)
    - **Description:** Developed a Decision Tree classification model to evaluate car acceptability (unacc, acc, good, vgood) based on categorical attributes such as safety, price, maintenance cost, and passenger capacity.
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Graphviz, Decision Tree Classifier
    - **Results:** After applying ordinal encoding, class weighting, and cost-complexity pruning, the tuned Decision Tree achieved ~99.5% test accuracy with improved generalization and reduced overfitting.
   
4. [**Decision Tree Classifier on Iris Dataset**](https://github.com/PranayDomal/Machine-Learning-Projects/tree/main/DecisionTree-Iris_Dataset)
    - **Description:** Built an interpretable Decision Tree classification model to predict Iris flower species (Setosa, Versicolor, Virginica).
    - **Technologies Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Decision Tree Classifier
    - **Results:** Achieved 95.56% test accuracy, with perfect classification of Iris Setosa and minor confusion between Versicolor and Virginica.

---

## Skills Demonstrated
- Exploratory Data Analysis (EDA)
- Feature Selection & Scaling
- Supervised & Unsupervised Learning
- Model Evaluation & Interpretation
- Business-Oriented Insights

---

## Feedback and Contact

I welcome any feedback, suggestions, or questions you may have about the projects or any kind of sponsorships for the repository. Feel free to reach out to me via 

- GitHub: https://github.com/PranayDomal
- LinkedIn: https://www.linkedin.com/in/pranay-domal-a641bb368
- Email: domalpranay@gmail.com

Enjoy exploring my machine learning projects!
