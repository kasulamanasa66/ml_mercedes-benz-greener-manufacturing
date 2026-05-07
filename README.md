# ml_mercedes-benz-greener-manufacturing
Applied Machine Learning project using PCA and regression techniques on Mercedes-Benz manufacturing data.


🚗 Mercedes-Benz Greener Manufacturing

Machine Learning project to predict the testing time of cars in the Mercedes-Benz production pipeline using multiple regression and ensemble learning techniques.

📌 Problem Statement

Mercedes-Benz aims to reduce the time cars spend on the test bench during manufacturing.
The objective of this project is to build a Machine Learning model that can accurately predict testing time (y) based on various anonymized features.

Reducing testing time helps:

improve manufacturing efficiency
reduce carbon emissions
optimize resource utilization

🎯 Objective

Build and compare multiple Machine Learning regression models using:

Dimensionality Reduction (PCA)
Regularization Techniques
Ensemble Learning
Cross Validation

The goal is to identify the model with the best generalization performance.

🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
XGBoost

📂 Dataset
The dataset contains anonymized categorical and numerical features.
Files used:
train.csv
test.csv

Target Variable:
y → testing time

⚙️ Techniques Applied

✅ Data Preprocessing
Removed ID column
Label Encoding for categorical features
Removed Columns with zero variance
Feature Scaling using StandardScaler

✅ Dimensionality Reduction

Applied Principal Component Analysis (PCA):
Purpose:
reduce dimensionality
remove redundancy
retain 95% variance
✅ Cross Validation
Used 5-Fold Cross Validation for robust evaluation.
Benefits:
better generalization
reduced overfitting
stable model evaluation

Models Used

1. Linear Regression
Baseline regression model.
2. Lasso Regression
Linear Regression with L1 Regularization.
3. Ridge Regression
Linear Regression with L2 Regularization.
4. ElasticNet
Combination of L1 and L2 regularization.
5. Random Forest Regressor
Bagging-based ensemble learning model.
7. XGBoost Regressor
Boosting-based ensemble learning model with regularization.

📊 Evaluation Metrics

The following metrics were used:
R² Score
RMSE (Root Mean Squared Error)

| Model             | Avg Train R² | Avg Validation R² |
| ----------------- | ------------ | ----------------- |
| Linear Regression | 0.5721       | 0.5269            |
| Ridge Regression  | 0.5721       | 0.5270            |
| Lasso Regression  | 0.5720       | 0.5275            |
| ElasticNet        | 0.5721       | 0.5274            |
| Random Forest     | 0.6999       | 0.4751            |
| XGBoost           | 0.6418       | 0.5028            |

🔍 Key Observations
Regularized linear models performed best after PCA.
Lasso Regression achieved the highest validation R² score.
Random Forest and XGBoost showed signs of overfitting.


🧠 Conclusion

This project demonstrates how dimensionality reduction and regularization can improve model generalization.

Key findings:

PCA transformed the feature space into a more linear representation.
Linear Model and Regularized models almost provide same accuracy.
linear models generalized better than ensemble models.
Ensemble models overfitted after dimensionality reduction.

📁 Output

The project generates:

Cross-validation metrics
Model comparison results
Submission CSV file (consisting of test IDs and corresponding predicted target value)
