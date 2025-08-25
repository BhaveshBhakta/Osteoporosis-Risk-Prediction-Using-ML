## Osteoporosis Risk Prediction

### Project Overview

This project aims to predict the **risk of osteoporosis** based on a variety of lifestyle and health factors. By analyzing features such as age, gender, hormonal changes, family history, body weight, and physical activity, the goal is to develop a machine learning model that can accurately classify an individual's osteoporosis risk. This can be a valuable tool for preventative healthcare and early risk assessment.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Lifestyle Factors Influencing Osteoporosis](https://www.kaggle.com/datasets/amitvkulkarni/lifestyle-factors-influencing-osteoporosis)
  * **Size**: 1958 entries, 16 columns
  * **Key Features**:
      * **Demographics**: `Age`, `Gender`.
      * **Health & Lifestyle**: `Hormonal Changes`, `Family History`, `Body Weight`, `Calcium Intake`, `Vitamin D Intake`, `Physical Activity`, `Smoking`.
      * **Medical History**: `Medical Conditions`, `Medications`, `Prior Fractures`.
  * **Approach**:
      * **Data Cleaning**: The `Id` column was dropped. Missing values in `Alcohol Consumption`, `Medical Conditions`, and `Medications` were handled by imputation. Specifically, `Alcohol Consumption` and `Medications` were filled with 'No', and `Medical Conditions` with 'No' after encoding.
      * **Exploratory Data Analysis**: Histograms, pie charts, and box plots were used for visualization to understand data distributions and relationships. The dataset is perfectly balanced with 979 cases for each class.
      * **Label Encoding**: Applied to all columns, converting categorical and numerical features into a format suitable for the models.
      * **Standard Scaling**: The 'Age' column was standardized using `StandardScaler`.
      * **Binary Classification**: The target variable `Osteoporosis` indicates the presence (`1`) or absence (`0`) of the condition.
      * **Models Used**:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * **90.8%** with Gradient Boosting Classifier.
      * **89.0%** with Bagging Classifier.
      * **86.7%** with XGBoost Classifier.

-----

### Purpose and Applications

  * Assist medical professionals in **early risk assessment for osteoporosis**.
  * Identify individuals at high risk for osteoporosis to recommend preventive measures and lifestyle changes.
  * Support public health initiatives by enabling a better understanding of osteoporosis risk factors.
  * Provide a tool for educational purposes in bone health and data analysis.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Osteoporosis-Risk-Prediction-Using-ML.git
cd Osteoporosis-Risk-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning and cross-validation for all models to ensure robustness.
  * Exploring more robust imputation strategies for the missing data in `Alcohol Consumption`, `Medical Conditions`, and `Medications`.
  * Investigating the impact of different feature selection or transformation techniques on model performance.
  * Adding explainability (e.g., SHAP or LIME) to understand which health and lifestyle factors are the most critical for osteoporosis risk prediction.
